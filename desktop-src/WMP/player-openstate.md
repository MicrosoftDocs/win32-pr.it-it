---
title: Player.openState
description: La proprietà openState recupera un valore che indica lo stato dell'origine di contenuto.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player.openState Windows Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7c0b88d3cab5d5bae4efb1e9a2a5032709943d82484b073302bf0b45a6f5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995981"
---
# <a name="playeropenstate"></a>Player.openState

La **proprietà openState** recupera un valore che indica lo stato dell'origine di contenuto.

## <a name="syntax"></a>Sintassi

*lettore* . **openState**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero **di sola lettura** (**long**). La costante di enumerazione di tipo C può essere derivata anteporre "wmpos" al valore dello stato. Ad esempio, la costante per lo stato PlaylistOpening è **wmposPlaylistOpening**.



| Valore | State                   | Descrizione                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non definito               | Windows Media Player è in uno stato non definito.                                                                                                         |
| 1     | PlaylistChanging        | La nuova playlist sta per essere caricata.                                                                                                                    |
| 2     | PlaylistLocazione        | Windows Media Player sta tentando di individuare la playlist. La playlist può essere locale (libreria o metafile con estensione asx) o remota. |
| 3     | PlaylistConnessione      | Connessione alla playlist.                                                                                                                            |
| 4     | PlaylistCaricamento         | La playlist è stata trovata ed è in corso il recupero.                                                                                                    |
| 5     | PlaylistApertura         | La playlist è stata recuperata e viene ora analizzata e caricata.                                                                                        |
| 6     | PlaylistOpenNoMedia     | La playlist è aperta.                                                                                                                                      |
| 7     | PlaylistChanged         | A **currentPlaylist** è stata assegnata una nuova playlist.                                                                                               |
| 8     | MediaChanging           | Sta per essere caricato un nuovo elemento multimediale.                                                                                                                |
| 9     | MediaLocating           | Windows Media Player sta individuando l'elemento multimediale. Il file può essere locale o remoto.                                                                      |
| 10    | MediaConnecting         | Connessione al server che contiene l'elemento multimediale.                                                                                                    |
| 11    | MediaLoading            | L'elemento multimediale è stato individuato ed è in corso il recupero.                                                                                                |
| 12    | MediaOpening            | L'elemento multimediale è stato recuperato ed è in corso l'apertura.                                                                                                 |
| 13    | MediaOpen               | L'elemento multimediale è ora aperto.                                                                                                                                |
| 14    | BeginCodecAcquisition   | Avvio dell'acquisizione del codec.                                                                                                                            |
| 15    | EndCodecAcquisition     | L'acquisizione del codec è stata completata.                                                                                                                         |
| 16    | BeginLicenseAcquisition | Acquisizione di una licenza per riprodurre contenuto protetto da DRM.                                                                                                     |
| 17    | EndLicenseAcquisition   | La licenza per la riproduzione di contenuto protetto da DRM è stata acquisita.                                                                                               |
| 18    | BeginIndividualization  | Iniziare l'individualizzazione DRM.                                                                                                                           |
| 19    | EndIndividualization    | L'individualizzazione DRM è stata completata.                                                                                                              |
| 20    | MediaWaiting            | In attesa dell'elemento multimediale.                                                                                                                                |
| 21    | OpeningUnknownURL       | Apertura di un URL di tipo sconosciuto.                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Windows Media Player non è garantito che gli stati si verifichino in un ordine specifico. Inoltre, non tutti gli stati si verificano necessariamente durante una sequenza di eventi. Non è consigliabile scrivere codice che si basa sull'ordine di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Evento Player.OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 





