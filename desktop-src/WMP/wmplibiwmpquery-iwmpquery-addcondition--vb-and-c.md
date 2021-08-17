---
title: Metodo IWMPQuery addCondition
description: Il metodo addCondition aggiunge una condizione alla query composta usando la logica AND.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- Metodo addCondition Windows Media Player
- Metodo addCondition Windows Media Player, interfaccia IWMPQuery
- Interfaccia IWMPQuery Windows Media Player , metodo addCondition
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe85999c60364827d483f81d14ff88602c9b2831c16e7cff8a3e17076b77671d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745706"
---
# <a name="iwmpqueryaddcondition-method"></a>Metodo IWMPQuery::addCondition

Il **metodo addCondition** aggiunge una condizione alla query composta usando la **logica AND.**

## <a name="syntax"></a>Sintassi


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAttribute* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nome dell'attributo da aggiungere alla query.

</dd> <dt>

*bstrOperator* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta l'operatore . Vedere Osservazioni per i valori supportati.

</dd> <dt>

*bstrValue* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il valore dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le condizioni contenute in una query composta sono organizzate in gruppi di condizioni. Più condizioni all'interno di un gruppo di condizioni vengono sempre concatenate usando la **logica AND.** I gruppi di condizioni vengono sempre concatenati tra loro usando la **logica OR.** Per avviare un nuovo gruppo di condizioni, chiamare [IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).

Per le query composte **che usano IWMPQuery** non viene fatto distinzione tra maiuscole e minuscole.

Un elenco di valori per il *parametro bstrAttribute* è disponibile in [Informazioni di riferimento per gli attributi alfabetici.](alphabetical-attribute-reference.md)

Nella tabella seguente sono elencati i valori supportati per *bstrOperator*.



| string              | Si applica a     |
|---------------------|----------------|
| BeginsWith          | Stringhe        |
| Contiene            | Stringhe        |
| Uguale a              | Tutti i tipi      |
| GreaterThan         | Numeri, date |
| GreaterThanOrEquals | Numeri, date |
| LessThan            | Numeri, date |
| LessThanOrEquals    | Numeri, date |
| NotBeginsWith       | Stringhe        |
| NotContains         | Stringhe        |
| NotEquals           | Tutti i tipi      |



 

## <a name="examples"></a>Esempio

L'esempio seguente crea una query, aggiunge due condizioni e la usa per estrarre i risultati della query come raccolta di stringhe. I risultati vengono quindi visualizzati in una casella di riepilogo. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi alfabetici**](alphabetical-attribute-reference.md)
</dt> <dt>

[**IWMPMediaCollection2.createQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getPlaylistByQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getStringCollectionByQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPQuery**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





