---
description: Binding di volumi e LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Binding di volumi e LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234412"
---
# <a name="volume-and-lun-binding"></a>Binding di volumi e LUN

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Il binding è la creazione di volumi o lun. I volumi sono costituiti da extent del disco e lun sono costituiti da extent di unità. L'associazione seleziona per un set di mapping a risorse fisiche e si verifica all'interno di un sottosistema, all'interno di un pacchetto o in entrambi. Tutti i programmi del provider supportano l'associazione parzialmente diretta a un modello in cui il chiamante specifica solo gli attributi di binding di particolare interesse e consente al provider di scegliere il resto. Le operazioni in VDS per l'associazione di volumi e lun sono simili, ma non identiche. I provider hardware possono ad esempio offrire opzioni di associazione aggiuntive.

VDS supporta i cinque tipi di binding di volumi e LUN seguenti per le configurazioni parzialmente dirette. I provider di hardware possono e supportano molte altre associazioni.



| Termine                                                                                                                                             | Descrizione                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Semplice<br/>                                                     | Mapping lineare con un solo extent contiguo.<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Con spanning<br/>                                                 | Mapping lineare con più extent non contigui tra più dischi o unità.<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Strisce<br/>                                                 | Mapping che interleave gli extent del volume contiguo tra più dischi o unità.<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Specchio<br/>                                             | Mapping che gestisce due o più copie di dati identiche.<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Con striping con parità<br/> | Mapping che distribuisce le informazioni di controllo della parità tra più dischi o unità.<br/>  |



 

VDS costruisce con mirroring, con striping e con striping con binding di parità da più di un membro. Ad esempio, un mirroring a due vie ha due membri. Ogni membro può occupare extent in più dischi o unità. VDS concatena gli extent per formare il membro, quindi associa il volume o il LUN sui membri. Un provider può supportare tutti i tipi di binding o qualsiasi subset. Nel modello a oggetti VDS ogni membro di un mirror è un oggetto indipendente denominato Plex.

Anche in questo caso i tipi di volume e LUN sono simili, ma non esatti. Per una descrizione dei tipi di volume, vedere l' [oggetto volume](volume-object.md); per i tipi LUN, vedere l' [oggetto lun](lun-object.md). I tipi di binding non sono a tolleranza d'errore o a tolleranza di errore.

### <a name="non-fault-tolerant-binding"></a>Associazione non a tolleranza di errore

I volumi e i LUN non a tolleranza di errore non offrono il ripristino di emergenza. Se uno degli assi che contribuiscono a un volume non a tolleranza di errore o a un LUN ha esito negativo, l'intero volume o LUN ha esito negativo. In Exchange il rischio per i dati, i volumi non a tolleranza di errore e i LUN offrono prestazioni di input/output generalmente superiori a quelle dei volumi e dei LUN a tolleranza di errore. VDS supporta i tre tipi non a tolleranza di errore seguenti: semplice, con spanning e con striping.

Semplice

![Diagramma che mostra un tipo semplice a tolleranza non di errore con 2 pacchetti e 2 sottosistemi.](images/vdssimplelunvol.png)

Spanned

![Diagramma che mostra un tipo non a tolleranza di errore con spanning con 1 pacchetto e 1 sottosistema.](images/vdsspanlunvol.png)

Strisce

![Diagramma che mostra un tipo a tolleranza non di errore con striping con 1 pacchetto e 1 sottosistema.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>Associazione a tolleranza di errore

I seguenti volumi di errore e lun offrono il ripristino di emergenza. Se uno degli assi che contribuiscono a un volume a tolleranza di errore o a un LUN ha esito negativo, è possibile recuperare i dati. In Exchange per la sicurezza dei dati, le prestazioni di input/output di volumi a tolleranza di errore e lun sono generalmente inferiori a quelle dei volumi e dei LUN non a tolleranza di errore. VDS supporta due tipi di tolleranza di errore: con mirroring e con striping con parità.

Con mirroring (mirroring a tre vie)

![Diagramma che mostra un tipo a tolleranza di errore con mirroring (mirroring a 3 vie).](images/vdsmirrorlunvol.png)

Con striping con parità

![Diagramma che mostra un tipo a tolleranza di errore con striping con parità.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica della configurazione](configuration.md)
</dt> <dt>

[Oggetto volume](volume-object.md)
</dt> <dt>

[LUN (oggetto)](lun-object.md)
</dt> </dl>

 

