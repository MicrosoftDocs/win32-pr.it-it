---
title: Metodo External.changeView
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato. Il metodo changeView modifica la visualizzazione in Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- Metodo changeView Windows Media Player
- Metodo changeView Windows Media Player , classe external
- Classe esterna Windows Media Player , metodo changeView
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa982e87e0a25fa8ae6cc80b428524844f60e2ec76f50d246e7b2a76b3ca942a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649371"
---
# <a name="externalchangeview-method"></a>Metodo External.changeView

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

Il **metodo changeView** modifica la visualizzazione in Windows Media Player.

## <a name="syntax"></a>Sintassi


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LibraryLocationType* \[ Pollici\]
</dt> <dd>

Costante [del percorso della](library-location-constants.md) libreria che specifica il tipo della nuova vista. Ad esempio, la costante CPGenreID specifica che la nuova vista mostrerà un particolare genere.

</dd> <dt>

*LibraryLocationID* \[ Pollici\]
</dt> <dd>

**Stringa** contenente l'ID dell'elemento specifico da visualizzare nella nuova visualizzazione. Ad esempio, se *LibraryLocationType* è CPGenreID, questo parametro specifica l'ID del genere da visualizzare nella nuova visualizzazione. Questa stringa può essere vuota. Vedere la sezione Osservazioni.

</dd> <dt>

*Filtro* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il filtro per la nuova visualizzazione. La visualizzazione verrà filtrata come se l'utente avesse immesso questo testo nel controllo della rotellina del giocatore. Questa stringa può essere vuota.

</dd> <dt>

*Parametri visualizzazione* \[ Pollici\]
</dt> <dd>

**Stringa** contenente i Windows Media Player disponibili per la nuova pagina di individuazione visualizzata con la nuova visualizzazione. Questi parametri non vengono interpretati da Windows Media Player. Vengono creati dallo store online e hanno un significato solo per lo store online.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

In alcuni casi, è opportuno impostare il *parametro LibraryLocationID* sulla stringa vuota. Ad esempio, se si imposta il *parametro LibraryLocationType* su AllCPAlbumIDs, la nuova visualizzazione rappresenterà tutti gli album. Nessun singolo album sarà l'obiettivo della nuova visualizzazione, quindi non è necessario specificare un ID album nel *parametro LibraryLocationID.*

Il *parametro ViewParams* consente a una pagina di individuazione di comunicare con un'altra pagina di individuazione. Quando lo script in una pagina di individuazione chiama **changeView,** Windows Media Player regola l'interfaccia utente. Questa regolazione fa in modo che player chiami il metodo [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del plug-in per ottenere l'URL di una nuova pagina di individuazione. La stringa passata dalla pagina di individuazione originale nel *parametro ViewParams* non viene passata a **GetTemplate.** Tuttavia, la nuova pagina di individuazione può recuperare la *stringa ViewParams* chiamando [External.viewParameters](external-viewparameters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External.viewParameters**](external-viewparameters.md)
</dt> </dl>

 

 





