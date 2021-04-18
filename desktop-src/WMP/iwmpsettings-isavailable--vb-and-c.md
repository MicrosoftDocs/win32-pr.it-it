---
title: IWMPSettings. disavailable (VB e C)
description: La proprietà disavailable (il \_ metodo Get disavailable in C \) ottiene un valore che indica se è possibile eseguire un'azione specificata.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings. disavailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325442"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a>IWMPSettings. disavailable (VB e C#)

La proprietà **disavailable** (il metodo **get \_ disavailable** in C#) ottiene un valore che indica se è possibile eseguire un'azione specificata.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Parametri

*bstrItem*

**System. String** che corrisponde a uno dei valori seguenti.



| Valore              | Descrizione                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| avvio automatico          | Rileva se la proprietà AutoStart può essere impostata in modo da specificare che Windows Media Player avvia automaticamente la riproduzione. |
| Balance            | Individua se è possibile utilizzare la proprietà Balance per impostare il bilanciamento dello stereo.                                           |
| BaseURL            | Rileva se la proprietà baseURL può essere impostata in modo da specificare un URL di base.                                                |
| DefaultFrame       | Rileva se la proprietà defaultFrame può essere impostata in modo da specificare il frame predefinito.                                    |
| EnableErrorDialogs | Rileva se la proprietà enableErrorDialogs può essere impostata in modo da abilitare o disabilitare la visualizzazione delle finestre di dialogo di errore.        |
| GetMode            | Rileva se il metodo GetMode può essere utilizzato per recuperare il ciclo corrente o la modalità shuffle.                          |
| InvokeURLs         | Rileva se la proprietà invokeURLs può essere impostata in modo da specificare se gli eventi URL devono avviare un Web browser.         |
| Disattiva audio               | Individua se è possibile impostare la proprietà mute per specificare se l'output audio è on o off.                        |
| PlayCount          | Rileva se la proprietà playCount può essere impostata in modo da specificare il numero di volte in cui un elemento multimediale verrà riprodotto.                 |
| Tariffa               | Individua se è possibile impostare la proprietà rate per controllare la velocità di riproduzione.                                            |
| SetMode            | Individua se è possibile utilizzare il metodo semode per specificare il ciclo corrente o la modalità shuffle.                           |
| Volume             | Individua se è possibile impostare la proprietà volume per specificare il volume audio.                                           |



 

## <a name="property-value"></a>Valore della proprietà

Valore **System. Boolean** che indica se è possibile eseguire l'azione specificata.

## <a name="remarks"></a>Commenti

**IWMPSettings. is identico** è una proprietà in Visual Basic che accetta un parametro. In C# viene indicato come il metodo **IWMPSettings. Get è \_ identico** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene testato ogni proprietà **IWMPSettings** utilizzando **la proprietà IsValid** (il metodo **get \_ unavailable** in C#). Il nome della proprietà e il risultato di ogni test vengono visualizzati in una casella di testo a più righe. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. AutoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Balance (VB e C#)**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB e C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. defaultFrame (VB e C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. getMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. mute (VB e C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. playCount (VB e C#)**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. rate (VB e C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. semode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. volume (VB e C#)**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





