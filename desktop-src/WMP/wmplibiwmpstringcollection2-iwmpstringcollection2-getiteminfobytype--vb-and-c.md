---
title: Metodo IWMPStringCollection2 getItemInfobyType
description: Il metodo getItemInfoByType restituisce il valore corrispondente all'indice dell'elemento della raccolta di stringhe, al nome, alla lingua e all'indice dell'attributo specificati.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- Metodo getItemInfobyType Windows Media Player
- Metodo getItemInfobyType Windows Media Player, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player, metodo getItemInfobyType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331726"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>Metodo IWMPStringCollection2:: getItemInfobyType

Il metodo **getItemInfoByType** restituisce il valore corrispondente all'indice dell'elemento della raccolta di stringhe, al nome, alla lingua e all'indice dell'attributo specificati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lCollectionIndex* \[ in\]
</dt> <dd>

**System. Int32** che rappresenta l'indice in base zero dell'elemento della raccolta di stringhe da cui ottenere l'attributo.

</dd> <dt>

*bstrType* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo.

</dd> <dt>

*bstrLanguage* \[ in\]
</dt> <dd>

**System. String** che indica il linguaggio. Se il valore è impostato su null o su una stringa di lunghezza zero (""), viene utilizzata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".

</dd> <dt>

*lAttributeIndex* \[ in\]
</dt> <dd>

**System. Int32** che rappresenta l'indice in base zero dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**Oggetto System. Object** che rappresenta l'elemento della raccolta di stringhe.

## <a name="remarks"></a>Commenti

Questo metodo supporta attributi con più valori e attributi con valori complessi. Il metodo **GetItemInfo** non supporta attributi con più valori o attributi con valori complessi.

Passando il valore "Child ' nel parametro *bstrType* , è possibile recuperare una nuova raccolta di stringhe che contiene gli elementi figlio di uno degli elementi nella raccolta di stringhe padre. Se, ad esempio, la raccolta padre contiene un elenco di AlbumIDs, è possibile usare questo metodo per ottenere una raccolta di stringhe figlio contenente tutte le tracce per uno degli album. Questo approccio è più rapido ed efficiente rispetto alla chiamata del metodo **IWMPMediaCollection2. getStringCollectionByQuery** due volte; una volta per ottenere una raccolta di AlbumIDs e una seconda volta per ottenere una raccolta di tracce per un determinato AlbumID. Per utilizzare l'elemento figlio nel modo appena descritto, è necessario che la raccolta di stringhe padre venga ottenuta da una raccolta di supporti tramite **IWMPLibraryServices** e non tramite la proprietà **AxWindowsMediaPlayer. mediacollection** .

Quando si utilizza l'elemento figlio, passare il valore "Child ' nel parametro *bstrType* e il valore 0 nel parametro *lAttributeIndex* . È quindi possibile eseguire il cast dell'oggetto restituito a un'interfaccia **IWMPStringCollection2** per accedere all'elenco figlio.

Per utilizzare questo metodo, è necessario disporre dell'accesso in lettura alla raccolta. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributo AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Interfaccia IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPStringCollection2**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfo (VB e C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





