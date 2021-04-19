---
title: Metodo WebHelp IWMPError
description: Il metodo WebHelp avvia la pagina della Guida Web di Windows Media Player per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero). | Metodo WebHelp IWMPError
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- Metodo WebHelp Media Player Windows
- Metodo WebHelp Media Player Windows, interfaccia IWMPError
- Interfaccia IWMPError Windows Media Player, metodo Webhelp
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
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332434"
---
# <a name="iwmperrorwebhelp-method"></a>Metodo IWMPError:: Webhelp

Il metodo **WebHelp** avvia la pagina della Guida Web di Windows Media Player per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero).

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

Le pagine della Guida Web contengono sempre le informazioni più recenti e dettagliate sugli errori di Windows Media Player. Questo metodo trasferisce automaticamente le altre informazioni richieste dalla guida Web, ad esempio la versione del sistema operativo in uso.

Per accedere direttamente alle pagine della Guida Web, usare il codice di errore e i collegamenti di Support Center seguenti:

-   [Informazioni sul codice di errore di Windows Media Player](https://support.microsoft.com/kb/886273)
-   [Centro soluzioni Windows Media Player](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un pulsante che avvia la pagina della Guida Web di Microsoft Windows Media Player nel browser. L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





