---
description: Il formato VHD (Virtual Hard Disk) è una specifica di formato immagine disponibile pubblicamente che consente l'incapsulamento del disco rigido in un singolo file per l'uso da parte del sistema operativo come disco virtuale nello stesso modo in cui vengono usati i dischi rigidi fisici.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Informazioni sul disco rigido virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79bd7695144811a1ec98f79e736760bbaddc8ef4b7460e55c5a66353a0b2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865957"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>Informazioni sul disco rigido virtuale

Il formato VHD (Virtual Hard Disk) è [](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) una specifica di formato immagine disponibile pubblicamente che consente l'incapsulamento del disco rigido in un singolo file per l'uso da parte del sistema operativo come disco virtuale *nello* stesso modo in cui vengono usati i dischi rigidi fisici. Questi dischi virtuali sono in grado di ospitare file system nativi (NTFS, FAT, exFAT e UDFS) supportando al tempo stesso operazioni su dischi e file standard. Il supporto dell'API VHD consente la gestione dei dischi virtuali. I dischi virtuali creati con l'API VHD possono funzionare come dischi di avvio.

Un esempio di come vengono usati i file VHD è la funzionalità [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) in Windows 7, Windows Server 2008, Virtual Server e Windows Virtual PC. Questi prodotti usano l'API VHD per contenere Windows'immagine del sistema operativo utilizzata da una macchina virtuale come disco di avvio del sistema.

Microsoft Windows Software Development Kit (SDK) integra il supporto VHD nativo per l'uso di dischi virtuali, semplificando la creazione, la gestione e la distribuzione di immagini Windows nei file VHD tramite il supporto api della piattaforma o gli strumenti di gestione. Non è necessario installare applicazioni separate o implementare un parser di formato VHD per abilitare queste operazioni. Queste API consentono l'uso generico dei dischi virtuali indipendentemente da qualsiasi altra tecnologia di virtualizzazione.

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminologia

Il termine *archivio di backup* viene usato per fare riferimento al file fisico presente nel disco rigido effettivo. L'archivio di backup è rappresentato da un *file di immagine del disco rigido virtuale*.

I termini *dinamico,* *espandibile* e *sparse* vengono spesso usati in modo intercambiabile quando si fa riferimento a dischi virtuali espandibili dinamicamente. Per la tecnologia VHD, questi termini sono identici.

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Panoramica delle funzionalità del sistema VHD

Il diagramma seguente presenta una panoramica delle funzionalità del disco rigido virtuale e delle relative relazioni.

![Diagramma a blocchi vhd](images/vhd.png)

Di seguito è riportata una spiegazione di riepilogo delle funzionalità descritte in precedenza.

API native Windows modalità utente:

-   VirtDisk.dll: libreria comune per le API di gestione del disco rigido virtuale.

Wrapper di gestione specifici del dominio in modalità utente:

-   [API VHD VHD](/windows/desktop/VDS/about-vds) : wrapper del modello a oggetti VDS per le API Windows VHD.

Driver in modalità kernel:

-   VDrvRoot.sys: enumeratore unità virtuale radice.
-   FsDepends.sys: gestione delle dipendenze dei volumi annidate.
-   Vhdmp.sys: parser VHD e provider di proprietà di dipendenza.

La documentazione dell'SDK in questa sezione illustra le API native Windows VHD.

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Tipi di dischi virtuali

Esistono considerazioni sull'uso dei dischi virtuali e sui tipi di dischi virtuali disponibili:

-   **Risolto:** il file di immagine del disco rigido virtuale è preallocato nell'archivio di backup per le dimensioni massime richieste.
-   **Espandibile:** noto anche come "dinamico", "espandibile dinamicamente" e "sparse", il file di immagine del disco rigido virtuale usa solo la quantità di spazio nell'archivio di backup necessaria per archiviare i dati effettivi attualmente contenuti nel disco virtuale. Quando si crea questo tipo di disco virtuale, l'API VHD non verifica la disponibilità di spazio libero sul disco fisico in base alle dimensioni massime richieste, pertanto è possibile creare correttamente un disco virtuale dinamico con dimensioni massime maggiori dello spazio disponibile su disco fisico. Per altre informazioni, vedere [**ExpandVirtualDisk.**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk)
    **Nota**  Le dimensioni massime di un disco virtuale dinamico sono 2.040 GB.

     

-   **Differenze:** come base di questo tipo viene usato un disco virtuale padre, con eventuali scritture successive scritte nel disco virtuale come differenze nel nuovo file di immagine del disco rigido virtuale differenze e il file di immagine del disco rigido virtuale padre non viene modificato. Ad esempio, se si dispone di un disco virtuale del sistema operativo di avvio del sistema pulito come padre e si designa il disco virtuale differenze come disco virtuale corrente da usare per il sistema, il sistema operativo nel disco virtuale padre rimane nello stato originale per il ripristino rapido o per la creazione rapida di più immagini di avvio in base a dischi virtuali differenze aggiuntive. Per altre informazioni, vedere [**MergeVirtualDisk.**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk)
    **Nota**  La dimensione massima di un disco virtuale differenze è di 2.040 GB.

     

Tutti i tipi di disco virtuale hanno una dimensione minima di 3 MB.

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Argomenti correlati

[Informazioni su VDS](/windows/desktop/VDS/about-vds)

[Informazioni di riferimento sul disco rigido virtuale](vhd-reference.md)

[Specifica del formato dell'immagine del disco rigido virtuale](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
