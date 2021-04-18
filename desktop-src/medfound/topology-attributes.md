---
description: Attributi della topologia
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Attributi della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286b6dbfe922461083b49d77ad2351e98d562d3b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322026"
---
# <a name="topology-attributes"></a>Attributi della topologia

Gli attributi seguenti si applicano alle topologie.



| Attributo                                                                                                | Descrizione                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Modalità DXVA topologia MF \_ \_](mf-topology-dxva-mode.md)                                                    | Specifica se il caricatore della topologia Abilita Microsoft DirectX Video Acceleration (DXVA) nella topologia.                                                                                                                         |
| [\_modifica dinamica della topologia MF \_ \_ \_ non \_ consentita](mf-topology-dynamic-change-not-allowed.md)                | Specifica se la sessione multimediale tenta di modificare la topologia quando il formato di un flusso viene modificato.                                                                                                                           |
| [\_ \_ Abilita \_ XVP per la topologia MF \_ per \_ la riproduzione](mf-topology-enable-xvp-for-playback.md)                | Specifica se il caricatore della topologia Abilita il processore del video transcodificato (XVP). per le conversioni, abilitazione della conversione di colori con accelerazione hardware.                                                                                        |
| [\_topologia MF \_ enumerazione di \_ tipi di origine \_](mf-topology-enumerate-source-types.md)                         | Specifica se il caricatore della topologia enumera i tipi di supporto forniti dall'origine multimediale.                                                                                                                                     |
| [\_modalità hardware della topologia MF \_ \_](mf-topology-hardware-mode.md)                                            | Specifica se includere le trasformazioni basate su hardware nella topologia.                                                                                                                                                            |
| [**\_topologia MF \_ senza \_ \_ contrassegno**](mf-topology-no-markin-markout-attribute.md)                     | Specifica se la pipeline esegue il trim degli esempi.                                                                                                                                                                                      |
| [\_framerate di riproduzione della topologia MF \_ \_](mf-topology-playback-framerate.md)                                  | Specifica la frequenza di aggiornamento del monitoraggio.                                                                                                                                                                                                |
| [MF \_ \_ massima riproduzione topologia \_ \_ Dim](mf-topology-playback-max-dims.md)                                   | Specifica le dimensioni della finestra di destinazione per la riproduzione video.                                                                                                                                                                   |
| [**\_PROJECTSTART topologia MF \_**](mf-topology-projectstart-attribute.md)                                 | Specifica l'ora di inizio della topologia all'interno del segmento corrente, in unità di 100 nanosecondi.                                                                                                                                             |
| [**\_PROJECTSTOP topologia MF \_**](mf-topology-projectstop-attribute.md)                                   | Specifica l'ora di arresto della topologia all'interno del segmento corrente, in unità di 100 nanosecondi.                                                                                                                                              |
| [**\_stato di risoluzione della topologia MF \_ \_**](mf-topology-resolution-status-attribute.md)                      | Specifica lo stato di un tentativo di risoluzione di una topologia.                                                                                                                                                                          |
| [\_ora di inizio della topologia MF \_ \_ \_ sull' \_ opzione di presentazione \_](mf-topology-start-time-on-presentation-switch.md) | Specifica l'ora di inizio per le presentazioni accodate dopo la prima presentazione.                                                                                                                                           |
| [\_ \_ \_ ottimizzazioni della riproduzione \_ statica della topologia MF](mf-topology-static-playback-optimizations.md)           | Abilita le ottimizzazioni statiche nella pipeline video.                                                                                                                                                                                |
| [\_Attributo di \_ sblocco \_ FIELDOFUSE MFT](mft-fieldofuse-unlock-attribute.md)                                | Contiene un puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , che viene usato per sbloccare un MFT con restrizioni di campo di utilizzo. Per ulteriori informazioni, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 



