---
description: Il formato del disco rigido virtuale (VHD) è una specifica del formato di immagine disponibile pubblicamente che consente di incapsulare il disco rigido in un singolo file per l'uso da parte del sistema operativo come disco virtuale in tutti gli stessi modi in cui vengono usati i dischi rigidi fisici.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Informazioni su VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751522"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>Informazioni su VHD

Il formato del disco rigido virtuale (VHD) è una [specifica](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) del formato di immagine disponibile pubblicamente che consente di incapsulare il disco rigido in un singolo file per l'uso da parte del sistema operativo come *disco virtuale* in tutti gli stessi modi in cui vengono usati i dischi rigidi fisici. Questi dischi virtuali sono in grado di ospitare file System nativi (NTFS, FAT, exFAT e UDF), supportando al tempo stesso le operazioni standard su disco e file. Il supporto delle API VHD consente la gestione dei dischi virtuali. I dischi virtuali creati con l'API VHD possono fungere da dischi di avvio.

Un esempio di come vengono usati i file VHD è la funzionalità [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) in Windows 7, windows Server 2008, Virtual Server e Windows Virtual PC. Questi prodotti usano l'API del disco rigido virtuale per contenere l'immagine del sistema operativo Windows usata da una macchina virtuale come disco di avvio del sistema.

Il Software Development Kit (SDK) di Microsoft Windows integra il supporto VHD nativo per l'utilizzo di dischi virtuali, semplificando la creazione, la gestione e la distribuzione di immagini di Windows in file VHD tramite gli strumenti di gestione o il supporto API della piattaforma. Non è necessario installare applicazioni separate o implementare un parser di formato VHD per abilitare queste operazioni. Queste API consentono l'uso generico di dischi virtuali indipendenti da qualsiasi altra tecnologia di virtualizzazione.

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminologia

Il termine *Archivio di backup* viene usato per fare riferimento al file fisico presente sul disco rigido effettivo. L'archivio di backup è rappresentato da un *file di immagine VHD*.

I termini *dinamici*, *espandibili* e *sparse* vengono spesso usati in modo interscambiabile quando si fa riferimento a dischi virtuali espandibili dinamicamente. Per la tecnologia VHD, questi termini sono identici.

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Panoramica delle funzionalità del sistema VHD

Il diagramma seguente presenta una panoramica delle funzionalità del disco rigido virtuale e delle relative relazioni.

![diagramma di blocco VHD](images/vhd.png)

Di seguito è riportata una spiegazione riepilogativa delle funzionalità descritte in precedenza.

API Windows native in modalità utente:

-   VirtDisk.dll libreria comune per le API di gestione del disco rigido virtuale.

Wrapper di gestione specifici del dominio in modalità utente:

-   [API del disco rigido virtuale VDS](/windows/desktop/VDS/about-vds) : wrapper del modello a oggetti VDS per le API Windows del disco rigido virtuale.

Driver in modalità kernel:

-   Enumeratore unità virtuale VDrvRoot.sys-root.
-   Gestione delle dipendenze del volume annidato in FsDepends.sys.
-   Parser Vhdmp.sys-VHD e provider di proprietà di dipendenza.

La documentazione dell'SDK in questa sezione descrive le API native di Windows VHD in modalità utente.

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Tipi di dischi virtuali

Ci sono alcune considerazioni per l'uso dei dischi virtuali e i tipi di dischi virtuali disponibili:

-   **Corretto**: il file di immagine del disco rigido virtuale è preallocato nell'archivio di backup per le dimensioni massime richieste.
-   **Espandibile**, noto anche come "dinamico", "espandibile in modo dinamico" e "sparse", il file di immagine VHD usa solo lo spazio disponibile nell'archivio di backup in base alle esigenze per archiviare i dati effettivi attualmente contenuti nel disco virtuale. Quando si crea questo tipo di disco virtuale, l'API VHD non verifica lo spazio disponibile sul disco fisico in base alle dimensioni massime richieste. è pertanto possibile creare correttamente un disco virtuale dinamico con dimensioni massime maggiori dello spazio libero su disco fisico disponibile. Per ulteriori informazioni, vedere [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).
    **Nota**  Le dimensioni massime di un disco virtuale dinamico sono di 2.040 GB.

     

-   **Differenze: un** disco virtuale padre viene utilizzato come base di questo tipo, con tutte le scritture successive scritte nel disco virtuale come differenze rispetto al nuovo file di immagine del disco rigido virtuale differenze e il file di immagine VHD padre non viene modificato. Ad esempio, se si dispone di un disco virtuale del sistema operativo di avvio del sistema con installazione pulita come padre e si designa il disco virtuale differenze come disco virtuale corrente per il sistema, il sistema operativo del disco virtuale padre rimane nello stato originale per il ripristino rapido o per creare rapidamente altre immagini di avvio basate su dischi virtuali differenze aggiuntivi. Per ulteriori informazioni, vedere [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).
    **Nota**  Le dimensioni massime di un disco virtuale differenze sono di 2.040 GB.

     

Tutti i tipi di dischi virtuali hanno una dimensione minima di 3 MB.

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Argomenti correlati

[Informazioni su VDS](/windows/desktop/VDS/about-vds)

[Riferimento al disco rigido virtuale](vhd-reference.md)

[Specifica del formato immagine del disco rigido virtuale](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
