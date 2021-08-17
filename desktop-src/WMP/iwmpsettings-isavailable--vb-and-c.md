---
title: IWMPSettings.isAvailable (VB e C )
description: La proprietà isAvailable (il metodo get isAvailable in C\ ) ottiene un valore che indica se è possibile eseguire \_ un'azione specificata.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings.isAvailable (VB e C ) Windows Media Player
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
ms.openlocfilehash: 590979677e79073466f7511b3f382a4bfcebc8bf0fd8ad4cb10f6dcd957db28a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135374"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a>IWMPSettings.isAvailable (VB e C#)

La **proprietà isAvailable** (il **metodo get \_ isAvailable** in C#) ottiene un valore che indica se è possibile eseguire un'azione specificata.


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

**System.String** che è uno dei valori seguenti.



| Valore              | Descrizione                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| avvio automatico          | Individua se la proprietà autoStart può essere impostata per specificare Windows Media Player la riproduzione automatica. |
| Balance            | Individua se la proprietà balance può essere usata per impostare il bilanciamento stereo.                                           |
| BaseURL            | Individua se la proprietà baseURL può essere impostata per specificare un URL di base.                                                |
| DefaultFrame       | Individua se la proprietà defaultFrame può essere impostata per specificare il frame predefinito.                                    |
| EnableErrorDialogs | Individua se la proprietà enableErrorDialogs può essere impostata per abilitare o disabilitare la visualizzazione di finestre di dialogo di errore.        |
| GetMode            | Individua se il metodo getMode può essere usato per recuperare il ciclo corrente o la modalità casuale.                          |
| InvokeURLs         | Individua se la proprietà invokeURLs può essere impostata per specificare se gli eventi URL devono avviare un Web browser.         |
| Disattiva audio               | Individua se la proprietà mute può essere impostata per specificare se l'output audio è on o off.                        |
| PlayCount          | Individua se la proprietà playCount può essere impostata per specificare il numero di volte in cui un elemento multimediale verrà riprodotto.                 |
| Tariffa               | Individua se la proprietà rate può essere impostata per controllare la velocità di riproduzione.                                            |
| SetMode            | Individua se il metodo setMode può essere usato per specificare la modalità loop o shuffle corrente.                           |
| Volume             | Individua se la proprietà volume può essere impostata per specificare il volume audio.                                           |



 

## <a name="property-value"></a>Valore della proprietà

Valore **System.Boolean** che indica se è possibile eseguire l'azione specificata.

## <a name="remarks"></a>Commenti

**IWMPSettings.isIdentical è** una proprietà in Visual Basic che accetta un parametro . In C# viene definito metodo **\_ isIdentical di IWMPSettings.get.**

## <a name="examples"></a>Esempio

L'esempio seguente verifica ogni **proprietà IWMPSettings** usando la proprietà **isAvailable** (il **metodo get \_ isAvailable** in C#). Il nome della proprietà e il risultato di ogni test vengono visualizzati in una casella di testo su più righe. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


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
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.balance (VB e C#)**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.baseURL (VB e C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.defaultFrame (VB e C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.getMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.invokeURLs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.mute (VB e C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.playCount (VB e C#)**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB e C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.setMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.volume (VB e C#)**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





