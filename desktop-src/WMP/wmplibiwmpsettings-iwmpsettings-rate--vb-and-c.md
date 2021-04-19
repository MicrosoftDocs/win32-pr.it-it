---
title: Proprietà frequenza IWMPSettings
description: La proprietà rate Ottiene o imposta la frequenza di riproduzione corrente per i video.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Media Player delle proprietà della frequenza
- Proprietà rate Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà rate
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
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325963"
---
# <a name="iwmpsettingsrate-property"></a>Proprietà IWMPSettings:: rate

La proprietà **rate** Ottiene o imposta la frequenza di riproduzione corrente per i video.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Valore proprietà

**System. Double** che corrisponde alla frequenza di riproduzione, con un valore predefinito di 1,0.

## <a name="remarks"></a>Commenti

Il valore recuperato da questa proprietà funge da valore moltiplicatore che consente di riprodurre un elemento multimediale a una velocità più veloce o più lenta. Il valore predefinito 1,0 indica la velocità creata.

Si noti che una traccia audio diventa difficile da comprendere a una velocità inferiore a 0,5 o superiore a 1,5. La velocità di riproduzione 2 indica il doppio della velocità di riproduzione normale.

Windows Media Player tenterà di utilizzare le quattro diverse modalità di riproduzione più efficaci delle seguenti.

-   Riproduzione video uniforme con il pitch audio mantenuto
-   Riproduzione video smussata con pitch audio non mantenuto
-   Riproduzione video senza audio
-   Riproduzione video del fotogramma chiave senza audio

La modalità scelta da Windows Media Player dipende da numerosi fattori, tra cui il tipo di file e la posizione, il sistema operativo, la rete e il server.

Si applicano anche altre considerazioni, a seconda del formato multimediale digitale usato per creare il contenuto:

-   **Windows Media Video (WMV) e ASF.** I valori ottimali per la proprietà **rate** sono compresi tra 1 e 10 o da 1 a 10 per la riproduzione inversa. Anche i valori compresi tra 0,5 e 1,0 o da-0,5 a-1,0 possono funzionare correttamente nei casi in cui è possibile mantenere il pitch audio, ad esempio quando si giocano file che si trovano nel computer locale. I valori con una grandezza assoluta maggiore di 10 sono consentiti, ma non sono molto significativi.
-   **Altri formati video.** La proprietà **rate** può variare da 0 a 9. I valori negativi non sono consentiti. I valori minori di 1 rappresentano un movimento lento. I valori superiori a 9 sono consentiti, ma non sono molto significativi.

Il metodo **IWMPControls. fastForward** modifica il valore di **rate** su 5,0, mentre il metodo **IWMPControls. fastReverse** modifica il valore di **rate** in 5,0.

Non è possibile modificare la velocità di riproduzione di alcuni formati multimediali digitali. Usare la proprietà **IWMPSettings.** IsValid (in C# il metodo **IWMPSettings. Get \_ unavailable** ) per individuare se questa proprietà può essere specificata per un particolare elemento multimediale.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato un controllo a discesa numerico che consente all'utente di modificare la velocità di riproduzione del supporto corrente. Quando l'utente fa clic sulle frecce verso l'alto o verso il basso del controllo, la proprietà **rate** viene impostata sul nuovo valore. Il possibile intervallo di valori nel controllo è 0,5 (metà velocità) a 2,0 (doppia velocità). L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPControls. fastForward (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastReverse (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. disavailable (VB e C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. mute (VB e C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





