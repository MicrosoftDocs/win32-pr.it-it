---
title: Metodo IWMPMedia getMarkerTime
description: Il metodo getMarkerTime restituisce l'ora del marcatore in corrispondenza dell'indice specificato.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- Metodo getMarkerTime Windows Media Player
- Metodo getMarkerTime Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player metodo , getMarkerTime
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293ad08137df1b87f47f614781d92be2b7c310fa7282cc234b38e1f3e0e63586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115693"
---
# <a name="iwmpmediagetmarkertime-method"></a>Metodo IWMPMedia::getMarkerTime

Il **metodo getMarkerTime** restituisce l'ora del marcatore in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*MarkerNum* \[ Pollici\]
</dt> <dd>

**System.Int32 che rappresenta** l'indice del marcatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System.Double che rappresenta** l'ora del marcatore.

## <a name="remarks"></a>Commenti

Questo metodo restituisce **NULL se** il marcatore specificato non esiste.

Alcuni elementi multimediali non contengono marcatori. Usare **markerCount per** individuare il numero di marcatori presenti nell'elemento multimediale corrente.

I numeri di indice dei marcatori iniziano da 1.

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

L'esempio di codice seguente **usa getMarkerTime** per riempire una casella di testo su più righe con la posizione di ogni marcatore. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

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

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.markerCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





