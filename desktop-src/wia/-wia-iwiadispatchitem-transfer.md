---
description: Il metodo di trasferimento dell'oggetto Item trasferisce i dati da un dispositivo a un file. Questo metodo si applica solo agli elementi del tipo di dispositivo.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308225"
---
# <a name="itemtransfer-method"></a>Item. Transfer (metodo)

Il metodo di **trasferimento** dell'oggetto [**Item**](-wia-item.md) trasferisce i dati da un dispositivo a un file. Questo metodo si applica solo agli elementi del tipo di dispositivo.

## <a name="syntax"></a>Sintassi


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome del file in cui vengono trasferiti i dati.

</dd> <dt>

*AsyncTransfer* \[ in\]
</dt> <dd>

Tipo: **Variant \_ bool**

Valore booleano che specifica se il trasferimento deve essere eseguito come chiamata asincrona.

<dt>



 (Variante \_ BOOL


</dt> <dd>

Valore predefinito. Impostare questo valore su **true** se la chiamata deve essere asincrona (vedere la **sezione Osservazioni**).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo si applica solo agli elementi di tipo file. Il metodo verifica che l'elemento supporti questo metodo prima di tentare di completare il trasferimento dei dati.

Usare "clipboard" come parametro *filename* per trasferire un elemento negli Appunti.

Impostare il valore *AsyncTransfer* su **false** per i trasferimenti all'interno di un'applicazione o di uno script in esecuzione in un ambiente che termina un processo alla fine di uno script, ad esempio Windows script host (WSH). In caso contrario, lo script può terminare e il processo viene terminato prima del completamento del trasferimento.

Il metodo di **trasferimento** non restituisce alcun valore. Al termine di un trasferimento, questo metodo invia un evento [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) allo script o all'applicazione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso del metodo di **trasferimento** per trasferire i dati da un dispositivo.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




