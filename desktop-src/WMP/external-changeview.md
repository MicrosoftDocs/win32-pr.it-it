---
title: External. changeView, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo changeView modifica la visualizzazione in Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- Metodo changeView Windows Media Player
- Metodo changeView Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo changeView
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
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324570"
---
# <a name="externalchangeview-method"></a>External. changeView, metodo

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **changeView** modifica la visualizzazione in Windows Media Player.

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

*LibraryLocationType* \[ in\]
</dt> <dd>

[Costante del percorso della libreria](library-location-constants.md) che specifica il tipo della nuova visualizzazione. Ad esempio, la costante CPGenreID specifica che la nuova vista mostrerà un genere particolare.

</dd> <dt>

*LibraryLocationID* \[ in\]
</dt> <dd>

**Stringa** contenente l'ID dell'elemento specifico da visualizzare nella nuova visualizzazione. Ad esempio, se *LibraryLocationType* è CPGenreID, questo parametro specifica l'ID del genere da visualizzare nella nuova visualizzazione. Questa stringa può essere vuota. Vedere la sezione Osservazioni.

</dd> <dt>

*Filtro* \[ di in\]
</dt> <dd>

**Stringa** contenente il filtro per la nuova visualizzazione. La vista verrà filtrata come se l'utente avesse immesso il testo nel controllo rotellina della parola del giocatore. Questa stringa può essere vuota.

</dd> <dt>

*ViewParams* \[ in\]
</dt> <dd>

**Stringa** contenente i parametri resi disponibili da Windows Media Player alla nuova pagina di individuazione visualizzata con la nuova visualizzazione. Questi parametri non vengono interpretati da Windows Media Player. Vengono creati dal negozio online e hanno un significato solo per lo Store online.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

In alcuni casi, è opportuno impostare il parametro *LibraryLocationID* sulla stringa vuota. Se ad esempio si imposta il parametro *LibraryLocationType* su AllCPAlbumIDs, la nuova vista rappresenterà tutti gli album. Nessun singolo album sarà l'obiettivo della nuova visualizzazione, quindi non è necessario fornire un ID album nel parametro *LibraryLocationID* .

Il parametro *ViewParams* consente a una pagina di individuazione di comunicare con un'altra pagina di individuazione. Quando script in una pagina di individuazione chiama **changeView**, Windows Media Player regola l'interfaccia utente. Tale modifica fa in modo che il lettore chiami il metodo [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del plug-in per ottenere l'URL di una nuova pagina di individuazione. La stringa che la pagina di individuazione originale passa nel parametro *ViewParams* non viene passata a **GetTemplate**. Tuttavia, la nuova pagina di individuazione può recuperare la stringa *ViewParams* chiamando [External. viewParameters](external-viewparameters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External. viewParameters**](external-viewparameters.md)
</dt> </dl>

 

 





