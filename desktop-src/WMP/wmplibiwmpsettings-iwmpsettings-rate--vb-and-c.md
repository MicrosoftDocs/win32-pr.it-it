---
title: Proprietà rate di IWMPSettings
description: La proprietà rate ottiene o imposta la frequenza di riproduzione corrente per il video.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Proprietà rate Windows Media Player
- Proprietà rate Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player , proprietà rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc053861b9061df676455e10b011cd0ffe0fe9f06052b129ec163e00d4c8d71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999701"
---
# <a name="iwmpsettingsrate-property"></a>Proprietà IWMPSettings::rate

La **proprietà rate** ottiene o imposta la frequenza di riproduzione corrente per il video.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Valore proprietà

**System.Double che** rappresenta la velocità di riproduzione, con un valore predefinito di 1,0.

## <a name="remarks"></a>Commenti

Il valore recuperato da questa proprietà funge da valore moltiplicatore che consente di riprodurre un elemento multimediale a una velocità più veloce o più lenta. Il valore predefinito 1,0 indica la velocità di creazione.

Si noti che una traccia audio diventa difficile da comprendere a velocità inferiori a 0,5 o superiori a 1,5. Una velocità di riproduzione di 2 indica il doppio della velocità di riproduzione normale.

Windows Media Player tenterà di usare la più efficace delle quattro diverse modalità di riproduzione seguenti

-   Riproduzione video uniforme con tono audio mantenuto
-   Riproduzione video uniforme con tono audio non mantenuto
-   Riproduzione video uniforme senza audio
-   Riproduzione di video con fotogrammi chiave senza audio

La modalità scelta dal Windows Media Player dipende da numerosi fattori, tra cui il tipo di file e la posizione, il sistema operativo, la rete e il server.

Si applicano anche altre considerazioni, a seconda del formato multimediale digitale usato per creare il contenuto:

-   **Windows Media Video (WMV) e ASF.** I valori ottimali per **la proprietà rate** sono da 1 a 10 o da 1 a 10 per la riproduzione inversa. I valori da 0.5 a 1.0 o da -0.5 a -1.0 possono essere validi anche nei casi in cui è possibile mantenere il passo audio, ad esempio durante la riproduzione di file che si trovano nel computer locale. I valori con grandezza assoluta maggiore di 10 sono consentiti, ma non sono molto significativi.
-   **Altri formati video.** La **proprietà rate** può variare da 0 a 9. I valori negativi non sono consentiti. I valori minori di 1 rappresentano un movimento lento. I valori superiori a 9 sono consentiti, ma non sono molto significativi.

Il **metodo IWMPControls.fastForward** modifica il valore di **rate** in 5.0, mentre il metodo **IWMPControls.fastReverse** modifica il valore di **rate** in 5.0.

Non è possibile modificare la velocità di riproduzione di alcuni formati multimediali digitali. Usare la **proprietà IWMPSettings.isAvailable** (in C# il metodo **IWMPSettings.get \_ isAvailable)** per determinare se questa proprietà può essere specificata per un particolare elemento multimediale.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzato un controllo di updown numerico che consente all'utente di modificare la velocità di riproduzione del contenuto multimediale corrente. Quando l'utente fa clic sulle frecce su o giù del controllo, la **proprietà rate** viene impostata sul nuovo valore. Il possibile intervallo di valori nel controllo è compreso tra 0,5 (velocità media) e 2,0 (doppia velocità). **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPControls.fastForward (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls.fastReverse (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.isAvailable (VB e C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.mute (VB e C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





