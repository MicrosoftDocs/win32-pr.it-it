---
description: Attributi della topologia
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Attributi della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db599a9d55e960bbb38043aa8932cd66ae0cbb6d9b376f403c1886faf3155c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972850"
---
# <a name="topology-attributes"></a>Attributi della topologia

Gli attributi seguenti si applicano alle topologie.



| Attributo                                                                                                | Descrizione                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MODALITÀ \_ \_ DXVA TOPOLOGIA MF \_](mf-topology-dxva-mode.md)                                                    | Specifica se il caricatore della topologia abilita Microsoft DirectX Video Acceleration (DXVA) nella topologia.                                                                                                                         |
| [MODIFICA DINAMICA DELLA TOPOLOGIA MF \_ \_ NON \_ \_ \_ CONSENTITA](mf-topology-dynamic-change-not-allowed.md)                | Specifica se la sessione multimediale tenta di modificare la topologia quando cambia il formato di un flusso.                                                                                                                           |
| [MF TOPOLOGY ENABLE XVP FOR PLAYBACK (TOPOLOGIA MF \_ \_ ABILITA \_ XVP \_ PER LA \_ RIPRODUZIONE)](mf-topology-enable-xvp-for-playback.md)                | Specifica se il caricatore della topologia abilita il processore video transcodifica (XVP). per le conversioni, abilitando la conversione dei colori accelerata dall'hardware.                                                                                        |
| [ENUMERARE I TIPI DI \_ \_ ORIGINE \_ DELLA \_ TOPOLOGIA MF](mf-topology-enumerate-source-types.md)                         | Specifica se il caricatore della topologia enumera i tipi di supporti forniti dall'origine multimediale.                                                                                                                                     |
| [MODALITÀ \_ HARDWARE DELLA TOPOLOGIA MF \_ \_](mf-topology-hardware-mode.md)                                            | Specifica se includere trasformazioni basate su hardware nella topologia.                                                                                                                                                            |
| [**TOPOLOGIA MF \_ \_ NO \_ MARKIN \_ MARKOUT**](mf-topology-no-markin-markout-attribute.md)                     | Specifica se la pipeline taglia gli esempi.                                                                                                                                                                                      |
| [FRAMERATE DI RIPRODUZIONE DELLA TOPOLOGIA MF \_ \_ \_](mf-topology-playback-framerate.md)                                  | Specifica la frequenza di aggiornamento del monitoraggio.                                                                                                                                                                                                |
| [MF \_ TOPOLOGY \_ PLAYBACK \_ MAX \_ DIMS](mf-topology-playback-max-dims.md)                                   | Specifica le dimensioni della finestra di destinazione per la riproduzione video.                                                                                                                                                                   |
| [**PROGETTO DI \_ TOPOLOGIA MFAVVIO \_**](mf-topology-projectstart-attribute.md)                                 | Specifica l'ora di inizio della topologia all'interno del segmento corrente, in unità da 100 nanosecondi.                                                                                                                                             |
| [**MF \_ TOPOLOGY \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md)                                   | Specifica il tempo di arresto della topologia all'interno del segmento corrente, in unità da 100 nanosecondi.                                                                                                                                              |
| [**STATO DELLA RISOLUZIONE DELLA TOPOLOGIA MF \_ \_ \_**](mf-topology-resolution-status-attribute.md)                      | Specifica lo stato di un tentativo di risolvere una topologia.                                                                                                                                                                          |
| [ORA DI INIZIO DELLA TOPOLOGIA MF \_ \_ \_ \_ ALL'INTERRUTTORE \_ \_ DI PRESENTAZIONE](mf-topology-start-time-on-presentation-switch.md) | Specifica l'ora di inizio per le presentazioni accodati dopo la prima presentazione.                                                                                                                                           |
| [OTTIMIZZAZIONI DELLA RIPRODUZIONE STATICA DELLA TOPOLOGIA \_ \_ \_ \_ MF](mf-topology-static-playback-optimizations.md)           | Abilita le ottimizzazioni statiche nella pipeline video.                                                                                                                                                                                |
| [Attributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                                | Contiene un [**puntatore IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) usato per sbloccare un MFT con restrizioni sul campo di utilizzo. Per altre informazioni, vedere [Field of Use Restrictions](field-of-use-restrictions.md). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Topologia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 



