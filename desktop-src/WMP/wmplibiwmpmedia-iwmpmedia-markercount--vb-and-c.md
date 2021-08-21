---
title: IWMPMedia markerCount - proprietà
description: La proprietà markerCount ottiene il numero di marcatori nell'elemento multimediale.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- Proprietà markerCount Windows Media Player
- Proprietà markerCount Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player proprietà , markerCount
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8afbc402858452c987bb6f2dcce0e1ad0428b8c67b81d2369de2a8cdbc6a7dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053629"
---
# <a name="iwmpmediamarkercount-property"></a>Proprietà IWMPMedia::markerCount

La **proprietà markerCount** ottiene il numero di marcatori nell'elemento multimediale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32 che rappresenta** il conteggio dei marcatori.

## <a name="remarks"></a>Commenti

Questa proprietà restituisce zero se un file non contiene marcatori o se l'elemento multimediale non corrisponde a quello specificato in AxWindowsMediaPlayer.currentMedia.

I numeri dei marcatori iniziano da 1.

Prima di usare questa proprietà, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

L'esempio seguente usa **markerCount** per recuperare il numero di marcatori nell'elemento multimediale corrente. Tale valore viene quindi usato come limite superiore per una struttura di ciclo, che scorre l'elenco dei marcatori per recuperare il nome di ogni marcatore e visualizzarlo in una casella di testo a più righe. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





