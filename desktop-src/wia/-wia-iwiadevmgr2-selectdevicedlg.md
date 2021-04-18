---
description: Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'Metodo IWiaDevMgr2:: SelectDeviceDlg (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cb41ec8e94782ee4d7408c53e2d4e098d986fe83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312415"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>Metodo IWiaDevMgr2:: SelectDeviceDlg

Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

Consente di specificare la finestra padre della finestra di dialogo **Seleziona dispositivo** .

</dd> <dt>

*lDeviceType* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica il tipo di dispositivo WIA 2,0 da usare. Per un elenco di valori possibili, vedere gli [identificatori del tipo di dispositivo WIA](-wia-wia-device-type-specifiers.md) .

</dd> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica il comportamento della finestra di dialogo. Il valore può essere uno dei seguenti.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Usare il comportamento predefinito

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ selezionare il \_ dispositivo \_ NODEFAULT**


</dt> <dd>

Visualizzare la finestra di dialogo anche se è presente un solo dispositivo corrispondente.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ in uscita\]
</dt> <dd>

Tipo: **BSTR \** _

Nell'output, riceve una stringa che contiene la stringa dell'identificatore del dispositivo. In fase di input, passare l'indirizzo di un puntatore se queste informazioni sono necessarie oppure _ *null** se non è necessario.

</dd> <dt>

*ppItemRoot* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento radice della struttura ad albero gerarchica che rappresenta il dispositivo WIA 2,0 selezionato. Se non viene trovato alcun dispositivo, riceve **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                                  | Descrizione                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | La selezione del dispositivo è stata completata. <br/>                                                          |
| <dl> <dt>**S \_ false**</dt> </dl>                      | L'utente ha annullato la finestra di dialogo. <br/>                                                              |
| <dl> <dt>**WIA \_ S \_ nessun \_ dispositivo \_ disponibile**</dt> </dl> | Nessun dispositivo hardware WIA 2,0 corrisponde alle specifiche specificate nel parametro *lDeviceType* . <br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo crea e visualizza la finestra di dialogo **Seleziona dispositivo** in modo che l'utente possa selezionare un dispositivo WIA 2,0 per l'acquisizione dell'immagine. Se un dispositivo viene selezionato correttamente, il metodo **IWiaDevMgr2:: SelectDeviceDlg** crea un albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) per il dispositivo. Archivia un puntatore all'interfaccia **IWiaItem2** dell'elemento radice nel parametro *ppItemRoot*.

L'applicazione può limitare i dispositivi visualizzati all'utente a determinati tipi specificando i tipi di dispositivo tramite il parametro *lDeviceType* . Se solo un dispositivo soddisfa la specifica, **IWiaDevMgr2:: SelectDeviceDlg** non Visualizza la finestra di dialogo **Seleziona dispositivo** . Viene invece creato l'albero [**IWiaItem2**](-wia-iwiaitem2.md) per il dispositivo e viene archiviato un puntatore all'interfaccia **IWiaItem2** dell'elemento radice nel parametro *ppItemRoot*. È possibile eseguire l'override di questo comportamento e forzare **IWiaDevMgr2:: SelectDeviceDlg** per visualizzare la finestra di dialogo specificando WIA \_ selezionare \_ Device \_ NODEFAULT come valore per il parametro *è* . Se più di un dispositivo WIA 2,0 corrisponde alla specifica, tutti i dispositivi corrispondenti vengono visualizzati nella finestra di dialogo **Seleziona dispositivo** , in modo che l'utente possa sceglierne uno.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppItemRoot* .

> [!Note]  
> È consigliabile che le applicazioni rendano disponibili la selezione del dispositivo e dell'immagine tramite una voce di menu denominata **da scanner** nel menu **file** .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
