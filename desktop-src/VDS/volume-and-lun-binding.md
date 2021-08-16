---
description: Associazione di volumi e LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Associazione di volumi e LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91014241014793b601c15c64ec19e5a2b1d153c71ba617cead54a5d68cf978b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125569"
---
# <a name="volume-and-lun-binding"></a>Associazione di volumi e LUN

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

L'associazione è la creazione di volumi o LUN. I volumi sono costituiti da extent del disco e LUN costituiti da extent di unità. L'associazione seleziona un set di mapping alle risorse fisiche e si verifica all'interno di un sottosistema, all'interno di un pacchetto o in entrambi. Tutti i programmi provider supportano l'associazione parzialmente diretta a un modello in cui il chiamante specifica solo gli attributi di associazione di particolare interesse e consente al provider di scegliere il resto. Le operazioni in VDS per l'associazione di volumi e LUN sono simili ma non identiche. Ad esempio, i provider hardware possono offrire opzioni di associazione aggiuntive.

VDS supporta i cinque tipi di associazione lun e volume seguenti per le configurazioni parzialmente indirizzate. I provider hardware possono e supportano molte altre associazioni.



| Termine                                                                                                                                             | Descrizione                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Semplice<br/>                                                     | Mapping lineare con un solo extent contiguo.<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Attraversato<br/>                                                 | Mapping lineare con più extent non contigui tra più dischi o unità.<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>a strisce<br/>                                                 | Mapping che consente di interfoliare gli extent di volumi contigui tra più dischi o unità.<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Specchio<br/>                                             | Mapping che gestisce due o più copie di dati identiche.<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striped con parità<br/> | Mapping che distribuisce le informazioni sul controllo di parità tra più dischi o unità.<br/>  |



 

VDS costruisce associazioni con mirroring, striped e striped con associazioni di parità da più di un membro. Ad esempio, un mirror bidiredetto ha due membri. Ogni membro può occupare extent in più dischi o unità. VDS concatena gli extent per formare il membro e quindi associa il volume o il LUN sui membri. Un provider può supportare tutti i tipi di associazione o qualsiasi subset. Nel modello a oggetti VDS ogni membro di un mirror è un oggetto indipendente denominato plex.

Anche in questo caso, i tipi di volume e LUN sono simili, ma non esatti. Per una descrizione dei tipi di volume, vedere [l'oggetto volume](volume-object.md). per i tipi LUN, vedere [l'oggetto LUN](lun-object.md). I tipi di associazione sono a tolleranza di errore o a tolleranza di errore.

### <a name="non-fault-tolerant-binding"></a>Associazione a tolleranza di errore

I volumi e i LUN non a tolleranza di errore non offrono il ripristino di emergenza. Se uno degli spindle che contribuisce a un volume a tolleranza di errore o un LUN non riesce, l'intero volume o LUN ha esito negativo. In cambio del rischio per i dati, i volumi e i LUN non a tolleranza di errore offrono prestazioni di input/output generalmente superiori a quella dei volumi e dei LUN a tolleranza di errore. VDS supporta i tre tipi a tolleranza di errore seguenti: semplice, con spanning e strip.

Semplice

![Diagramma che mostra un tipo semplice a tolleranza di errore con 2 Pack e 2 sottosistemi.](images/vdssimplelunvol.png)

Spanned

![Diagramma che mostra un tipo a tolleranza di errore con spanning con 1 pack e 1 sottosistema.](images/vdsspanlunvol.png)

a strisce

![Diagramma che mostra un tipo a tolleranza di errore senza striping con 1 pack e 1 sottosistema.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>Associazione a tolleranza di errore

I volumi e i LUN a tolleranza di errore seguenti offrono il ripristino di emergenza. Se uno degli spindle che contribuisce a un volume a tolleranza di errore o a un LUN ha esito negativo, i dati possono essere recuperati. In cambio della sicurezza dei dati, le prestazioni di input/output di volumi e LUN a tolleranza di errore sono in genere meno elevate rispetto a volumi e LUN non a tolleranza di errore. VDS supporta due tipi a tolleranza di errore: con mirroring e striped con parità.

Con mirroring (mirror a tre livelli)

![Diagramma che mostra un tipo a tolleranza di errore con mirroring (3-way).](images/vdsmirrorlunvol.png)

Striped con parità

![Diagramma che mostra un tipo a tolleranza di errore striped con parità.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica della configurazione](configuration.md)
</dt> <dt>

[Oggetto Volume](volume-object.md)
</dt> <dt>

[Oggetto LUN](lun-object.md)
</dt> </dl>

 

