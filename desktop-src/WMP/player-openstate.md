---
title: Player. openState
description: La proprietà openState recupera un valore che indica lo stato dell'origine del contenuto.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player. openState Windows Media Player
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
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324530"
---
# <a name="playeropenstate"></a>Player. openState

La proprietà **openState** recupera un valore che indica lo stato dell'origine del contenuto.

## <a name="syntax"></a>Sintassi

*Player* . **openState**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**). La costante di enumerazione di tipo C può essere derivata anteponendo il valore di stato con "wmpos". Ad esempio, la costante per lo stato PlaylistOpening è **wmposPlaylistOpening**.



| Valore | State                   | Descrizione                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non definito               | Windows Media Player è in uno stato non definito.                                                                                                         |
| 1     | PlaylistChanging        | La nuova playlist sta per essere caricata.                                                                                                                    |
| 2     | PlaylistLocating        | Windows Media Player sta tentando di individuare la playlist. La playlist può essere locale (libreria o metafile con estensione del nome di file ASX) o remota. |
| 3     | PlaylistConnecting      | Connessione alla playlist.                                                                                                                            |
| 4     | PlaylistLoading         | La playlist è stata trovata e ora è in fase di recupero.                                                                                                    |
| 5     | PlaylistOpening         | La playlist è stata recuperata e viene ora analizzata e caricata.                                                                                        |
| 6     | PlaylistOpenNoMedia     | La playlist è aperta.                                                                                                                                      |
| 7     | PlaylistChanged         | Una nuova playlist è stata assegnata a **currentPlaylist**.                                                                                               |
| 8     | MediaChanging           | Un nuovo elemento multimediale sta per essere caricato.                                                                                                                |
| 9     | MediaLocating           | Windows Media Player individua l'elemento multimediale. Il file può essere locale o remoto.                                                                      |
| 10    | MediaConnecting         | Connessione al server che include l'elemento multimediale.                                                                                                    |
| 11    | MediaLoading            | L'elemento multimediale è stato individuato e ora viene recuperato.                                                                                                |
| 12    | MediaOpening            | L'elemento multimediale è stato recuperato e ora è in fase di apertura.                                                                                                 |
| 13    | MediaOpen               | L'elemento multimediale è ora aperto.                                                                                                                                |
| 14    | BeginCodecAcquisition   | Avvio dell'acquisizione del codec.                                                                                                                            |
| 15    | EndCodecAcquisition     | L'acquisizione del codec è stata completata.                                                                                                                         |
| 16    | BeginLicenseAcquisition | Acquisizione di una licenza per riprodurre contenuti protetti da DRM.                                                                                                     |
| 17    | EndLicenseAcquisition   | È stata acquisita la licenza per la riproduzione di contenuti protetti da DRM.                                                                                               |
| 18    | BeginIndividualization  | Inizia l'individualizzazione DRM.                                                                                                                           |
| 19    | EndIndividualization    | L'individualizzazione DRM è stata completata.                                                                                                              |
| 20    | MediaWaiting            | In attesa dell'elemento multimediale.                                                                                                                                |
| 21    | OpeningUnknownURL       | Apertura di un URL con un tipo sconosciuto.                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare. Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi. Non è necessario scrivere codice che si basa sull'ordine di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Evento Player. OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 





