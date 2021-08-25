---
title: Metodo webHelp IWMPError
description: Il metodo webHelp avvia la Windows Media Player Guida Web per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero). | Metodo webHelp IWMPError
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- Metodo webHelp Windows Media Player
- Metodo webHelp Windows Media Player, interfaccia IWMPError
- Interfaccia IWMPError Windows Media Player, metodo webHelp
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d4b404988e8b317ec7b090adcb96aac8e26a5a82590aa1138848dc797e3e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115824"
---
# <a name="iwmperrorwebhelp-method"></a>Metodo IWMPError::webHelp

Il **metodo webHelp** avvia la Windows Media Player guida Web per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero).

## <a name="syntax"></a>Sintassi


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le pagine della Guida Web contengono sempre le informazioni più recenti e più dettagliate sugli Windows Media Player errore. Questo metodo trasferisce automaticamente le altre informazioni necessarie per la Guida Web, ad esempio la versione del sistema operativo in uso.

Per accedere direttamente alle pagine della Guida Web, usare il codice di errore e i collegamenti del supporto tecnico seguenti:

-   [Windows Media Player Informazioni sul codice di errore](https://support.microsoft.com/kb/886273)
-   [Windows Media Player Centro soluzioni](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Esempio

L'esempio seguente crea un pulsante che avvia la pagina Windows Media Player Guida Web di Microsoft nel browser. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

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

[**Interfaccia IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





