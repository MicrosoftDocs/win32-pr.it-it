---
title: External. changeViewOnlineList, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. changeViewOnlineList, metodo
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- Metodo changeViewOnlineList Windows Media Player
- Metodo changeViewOnlineList Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo changeViewOnlineList
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331233"
---
# <a name="externalchangeviewonlinelist-method"></a>External. changeViewOnlineList, metodo

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **changeViewOnlineList** modifica la visualizzazione in Windows Media Player per visualizzare un elenco generato dinamicamente dal negozio online.

## <a name="syntax"></a>Sintassi


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
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

**Stringa** contenente l'ID dell'elemento specifico da visualizzare nella nuova visualizzazione. Ad esempio, se *LibraryLocationType* è CPGenreID, questo parametro specifica l'ID del genere da visualizzare nella nuova visualizzazione. Questa stringa può essere vuota.

</dd> <dt>

*Parametri* \[ in\]
</dt> <dd>

**Stringa** contenente i parametri che Windows Media Player passa al plug-in del negozio online chiamando [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate). Questi parametri non vengono interpretati da Windows Media Player. Vengono creati dal negozio online e hanno un significato solo per lo Store online. Questa stringa può essere vuota

</dd> <dt>

*FriendlyName* \[ in\]
</dt> <dd>

**Stringa** contenente un nome descrittivo, che deve essere visualizzato da Windows Media Player per l'elenco dinamico.

</dd> <dt>

*ListType* \[ in\]
</dt> <dd>

Costante del percorso della libreria che specifica il tipo degli elementi nell'elenco generato dinamicamente. Se, ad esempio, il valore di questo parametro è CPTrackID, l'elenco dinamico conterrà le tracce.

</dd> <dt>

*ViewMode* \[ in\]
</dt> <dd>

**Stringa** che specifica la modalità utilizzata da Windows Media Player per visualizzare l'elenco dinamico. Il chiamante deve impostare questo parametro su uno dei valori seguenti, definiti in contentpartner. h:

ViewModeReport

ViewModeDetails

ViewModeIcon

ViewModeTile

ViewModeOrderedList

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando lo script in una pagina di individuazione chiama **changeViewOnlineList**, Windows Media Player passa alcuni dei parametri insieme ai metodi [IWMPContentPartner:: GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) e [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , implementati dal plug-in Online Store. Nella tabella seguente viene illustrata la corrispondenza tra i parametri dei tre metodi.



| parametro changeViewOnlineList | Parametro GetListContents | Parametro GetTemplate |
|--------------------------------|---------------------------|-----------------------|
| *LocationType*                 | *location*                | *location*            |
| *LocationID*                   | *pContext*                | *pContext*            |
| *Params*                       | *bstrParams*              | *bstrViewParams*      |
| *ListType*                     | *bstrListType*            | non applicabile        |



 

Poiché tutti e tre i metodi illustrati nella tabella precedente sono implementati dall'archivio online, è possibile usare i parametri in modo flessibile. L'idea è che si forniscano informazioni sufficienti per **GetListContents** per determinare l'elenco da recuperare e per **GetTemplate** per determinare la pagina di individuazione da visualizzare successivamente. Gli esempi seguenti illustrano due possibilità.

**Esempio 1: elenco dinamico presente nel catalogo del negozio online**

Si supponga di volere che il plug-in ottenga il contenuto dell'elenco dinamico con ID 6 nel catalogo del negozio online. Si supponga che l'elenco 6 sia un elenco di tracce. È possibile fornire il plug-in con informazioni sufficienti effettuando la chiamata seguente.


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



Si noti che il parametro *params* è vuoto; il plug-in dispone di informazioni sufficienti negli altri parametri.

**Esempio 2: elenco dinamico non presente nel catalogo del negozio online**

Si supponga di volere che il plug-in ottenga il contenuto di un elenco dinamico che non si trova nel catalogo del negozio online. Forse si è deciso di avere un elenco dinamico che include canzoni selezionate da un particolare artista. Si supponga che l'ID dell'artista sia 2 nel catalogo del negozio online. È possibile effettuare la chiamata seguente.


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



Si noti che i parametri *LocationType* e *LocationID* non specificano l'elenco. Il parametro *params* specifica invece l'elenco. I parametri *LocationType* e *LocationID* vengono passati a **IWMPContentPartner:: GetListContents**, ma in questo caso **GetListContents** possono ignorarli. I parametri *LocationType* e *LocationID* vengono passati anche a **IWMPContentPartner:: GetTemplate**, che può usarli per determinare la pagina di individuazione da visualizzare con l'elenco dinamico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartnerCallback::AddListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[**IWMPContentPartner:: GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**Posizione e elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 





