---
description: Costanti VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Costanti VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318208"
---
# <a name="vds-constants"></a>Costanti VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Le costanti VDS sono classificate come segue:

-   [Costanti di stato dell'oggetto](#object-status-constants)
-   [Costanti degli hint di automagic](#automagic-hints-constants)
-   [Costanti varie](#miscellaneous-constants)

### <a name="object-status-constants"></a>Costanti di stato dell'oggetto



| Costante           | Valore |
|--------------------|-------|
| STATO \_ sconosciuto    | 0     |
| STATO \_ online     | 1     |
| STATO \_ non \_ pronto | 2     |
| STATO \_ nessun \_ supporto  | 3     |
| STATO \_ offline    | 4     |
| STATO \_ non riuscito     | 5     |
| STATO \_ mancante    | 6     |



 

### <a name="automagic-hints-constants"></a>Costanti degli hint di automagic



| Costante                               | Valore   |
|----------------------------------------|---------|
| \_MOSTLYREADS hint \_ VDS                 | 0x0002L |
| \_OPTIMIZEFORSEQUENTIALREADS hint \_ VDS  | 0x0004L |
| \_OPTIMIZEFORSEQUENTIALWRITES hint \_ VDS | 0x0008L |
| \_REMAPENABLED hint \_ VDS                | 0x0020L |
| \_WRITETHROUGHCACHINGENABLED hint \_ VDS  | 0x0040L |
| \_HARDWARECHECKSUMENABLED hint \_ VDS     | 0x0080L |
| HINT VDS che è stato \_ \_ ritirato                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>Costanti varie



| Costante                     | Valore      |
|------------------------------|------------|
| \_min priorità di ricompilazione VDS \_ \_  | 0x0001L    |
| \_ \_ informazioni lun versione \_ VDS   | 1          |
| \_lunghezza max ComputerName \_    | 15         |
| \_lunghezza massima ProviderName \_    | 200        |
| \_lunghezza massima VERSIONSTRING \_   | 16         |
| \_prop lettera di unità \_          | N/D        |
| dimensioni MASSIMe del \_ \_ nome FS \_          | 8          |
| il \_ membro IDX non è valido \_         | 0xFFFFFFFF |
| \_ \_ lunghezza nome partizione \_ GPT | 36         |
| \_percorso massimo                    | 260        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento VDS](vds-reference.md)
</dt> </dl>

 

 
