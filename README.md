# Brian Downing

```
4114 Englewood Dr
Champaign, IL 61822-7710
bdowning@lavos.net
(217) 390-2945
```

*Software architect and programmer with a wide range of knowledge and
experience*

## Professional Work

### 2022–present: Paradromics

*Principal Software Engineer*

Developed software in support of brain computer interfaces.

- TODO

Primary technologies: Rust, Python

### 2018–2022: Granular

*Principal Software Engineer: 2019–2022; Staff Software Engineer: 2018–2019*

Designed and developed Granular Analysis, a system for analyzing,
correlating, and aggregating geospatial (raster) agronomic data and
associated financials.

- Presents a real-time query API to allow slicing and dicing data;
  this API is the source of most numbers and maps displayed in the
  Granular Insights product.
- Component of a larger system; data is ingested from several sources
  via AWS Kinesis streams and stored (in read-optimized form) in a
  Postgres database.  Rasters are stored in S3 and fetched
  just-in-time when API requests are made.
- Complex multi-dimensional queries are possible - "Show me my harvest
  yield and profit for 2022 corn binned by seed variety, planting
  date, harvest date, and soil type", "Show me harvest yield and area
  wherever I made less than $50/ac binned by year and crop type", etc.
- Compute is distributed - since single API queries can have
  farm-operation-wide visibility, lots of data may need to be fetched
  and processed to compute it.  Raster operations (which include
  actually fetching the rasters) are broken down into discrete work
  units which are dispatched to a compute cluster, initially
  implemented by HPA-scaled Kubernetes pods and eventually migrated
  to a somewhat novel system using Lambdas for compute for much faster
  scalability and decreased cost.
- A content-hash-based caching layer exists to prevent re-computing
  data multiple times.

Also participated in company-wide architecture and standardization
processes.

Primary technologies: Python, Postgres, Kubernetes, AWS

### 2012–2018: Independent Software Contracting

Various software development tasks, including the following:

1.  HBM, Inc.

    - Software development for EX23 IEEE1588- and POE-enabled switch
      product.
    - Extension of new (C++) DAQ infrastructure with fine-grained
      (coroutine) task switching capabilities to talk with extremely
      chatty legacy hardware.
    - Ongoing support and maintenance for eDAQ product.

    Primary technologies: C, C++(14), Lua

2.  Distant Focus Corp.

    - Creation of bytecode-based correction engine for bad image-sensor
      pixels.
    - Implemention of lens-distortion correction in WebGL.
    - Support for build systems and Lua FFI integration (see also
      <https://github.com/bdowning/lj-cdefdb>).

    Primary technologies: Lua, JavaScript

### 2012–2014: GLD, Inc.

*Cofounder, CTO*

- Conception, design, and implemention of software for USB- and
  Ethernet-based download box (based on TI AM1705) for locomotive
  event recorders, including build system, hardware bringup,
  bootloader, Linux port, all system and application software
  (including Web interface), and testing.

- Porting of third-party grain-dryer Internet remote control to new
  revision of AVR32 dev board.

Primary technologies: C, Lua, JavaScript

### 2000–2012: SoMat Corporation / nCode / HBM, Inc.

*Software Engineer*

Software/firmware development of portable rugged data acquisition
systems and surrounding infrastructure.

- Innumerable improvements and optimizations to eDAQ system software
  while producing customer releases for 10+ years.
- Design and implemention of libsie, a portable (Windows, Mac, Linux,
  embedded) C library for reading data from novel engineering data file
  format (SIE). Open-source (GPL), downloadable from hbm.com.
- Development of direct eDAQ video collection capabilities from IP
  cameras: Video is timestamped and correlated with engineering data and
  stored alongside in SIE file.
- Porting of eDAQ product from QNX to Linux; \~2x throughput
  improvement.
- Porting of eDAQ product from EOL'd AMD SC400 SOC to National
  Semiconductor Geode GX1, including hardware bringup.
- Integration of Lua runtime into C-based data acquisition engine,
  allowing rapid development of, amongst other things, new support for
  complicated vehicle-bus protocols.
- Migration of 10+ years of internal source code from CVS to Git.
- Primary design and architecture for components of next-generation
  data acquisition system, including build system for complete Linux
  toolchain and system.

Primary technologies: C, C++(98), Perl, Lua

### 2005–2006: Riverglass, Inc.

*Consultant*

Provided Common Lisp expertise to data analytics startup.

- Development of AI knowledgebase product implemented in Common Lisp and
  Postgres.

Primary technologies: Common Lisp, Postgres

### 1997–2000: Wolfram Research, Inc.

*Unix System Administrator; MathSource Administrator*

- Support and administration for a very heterogeneous collection of Unix
  machines.

- Implemention of company-wide automatic tape backup for critical Unix
  systems.

- Updating of MathSource web-based archive to be much more maintainable.

## Volunteer Work

### 1992–present: Monticello Railway Museum

*President: 2017–2020; Board Chairman: 2015–2017; Director: 2005–2012,
2014–2017*

Involvement with many activities at this not-for-profit educational
organization located in Monticello, IL, including train service,
mechanical work/machining, equipment restoration, special events, IT,
and management.

Technology-based accomplishments include:

- Design and implementation of Web-based system to automatically assign
  seating and print ticket envelopes and other materials for \~10,000
  Polar Express passengers per year. Integrated with online ticket
  vendor via API and local database mirror.

  Primary technologies: JavaScript, node.js, Postgres

- Design and implemention of automatic answering service for federally
  mandated grade-crossing Emergency Notification System (blue signs seen
  at railroad crossings). System answers phone, collects crossing number
  and records message from caller, then emails Museum operations staff
  and logs call.

  Primary technologies: JavaScript, node.js, Twilio

- Advanced music-synchronized lighting project for Polar Express event:

  - Design and manufacture of lighting with \~6,000 individually
    addressable LEDs for deluxe-class railcar.
  - Design and assembly of circuit boards and power distribution to
    drive the above.
  - Conception and implementation of in-band inaudible timecode
    transmitted with program music over train-wide PA, and software to
    extract timestamp.
  - Implementation of software to "play back" in realtime the
    appropriate light patterns based on music timestamp, distributed in
    10 channels over 3 Raspberry Pi's synchronized with IEEE1588.

  Primary technologies: C++(14), JavaScript, node.js, HTML5 Canvas,
  KiCad

- Finalization and implemention of demonstration railroad interlocking
  and signal system with historically accurate components (railroad
  relays).

  - Creation of tools to manage wiring assignments and print wiring tags
    for several thousand feet of wires between \~200 relays, circuit
    controllers, and signal apparatuses.
  - Creation of web-based circuit simulator to verify wiring netlist and
    debug system design before implementation.

  Primary technologies: JavaScript, React

- Network and Internet management and upgrades for 3 MRM sites, the
  primary of which is 1/2 mile long and served from a single Internet
  connection.

## Code, Open-Source Projects/Contributions

### Personal Projects

- sql-athame: <https://github.com/bdowning/sql-athame>
- opentracing-compose: <https://github.com/bdowning/opentracing-compose>
- lj-cdefdb: <https://github.com/bdowning/lj-cdefdb>
- ljev: <https://github.com/bdowning/ljev>
- retween: <https://github.com/bdowning/retween>
- sql-assassin: <https://github.com/bdowning/sql-assassin>
- liter: <https://github.com/bdowning/liter>

<!-- -->

- Personal Github: <https://github.com/bdowning/>
- MRM Github: <https://github.com/monticello-railway-museum/>

### Other Contributions

- Git: <https://git-scm.com/>
- SBCL: <http://www.sbcl.org/>
- SLIME: <https://github.com/slime/slime>
- ljsyscall: <https://github.com/justincormack/ljsyscall>
- lua-ev: <https://github.com/brimworks/lua-ev>
- rekapi: <https://github.com/jeremyckahn/rekapi>

<!-- -->

- Numerous bugfixes and miscellany in other open-source software.
