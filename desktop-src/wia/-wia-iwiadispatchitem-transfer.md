---
description: Il metodo Transfer dell'oggetto Item trasferisce i dati da un dispositivo a un file. Questo metodo si applica solo agli elementi di tipo dispositivo.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Metodo Item.Transfer
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
ms.openlocfilehash: efef054a324244553748b75659820f582100a01ed6f56f9a2f80b0ef0c08f105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706321"
---
# <a name="itemtransfer-method"></a>Metodo Item.Transfer

Il **metodo Transfer** dell'oggetto [**Item**](-wia-item.md) trasferisce i dati da un dispositivo a un file. Questo metodo si applica solo agli elementi di tipo dispositivo.

## <a name="syntax"></a>Sintassi


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome del file in cui vengono trasferiti i dati.

</dd> <dt>

*AsyncTransfer* \[ Pollici\]
</dt> <dd>

Tipo: **VARIANT \_ BOOL**

Valore booleano che specifica se il trasferimento deve essere eseguito come chiamata asincrona.

<dt>



 (VARIANT \_ BOOL)


</dt> <dd>

Valore predefinito. Impostare questo valore su **true** se la chiamata deve essere asincrona **(vedere la sezione Osservazioni).**

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo si applica solo agli elementi di tipo file. Il metodo verifica che l'elemento supporti questo metodo prima che tenti di completare il trasferimento dei dati.

Usare "clipboard" come parametro *Filename* per trasferire un elemento negli Appunti.

Impostare il *valore AsyncTransfer* su **false** per i trasferimenti all'interno di qualsiasi applicazione o script eseguito in un ambiente che termina un processo alla fine di uno script, ad esempio Windows Script Host (WSH). In caso contrario, lo script può terminare e il processo termina prima del completamento del trasferimento.

Il **metodo Transfer** non ha alcun valore restituito. Al termine di un trasferimento, questo metodo invia un [**evento OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) allo script o all'applicazione.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso del **metodo Transfer** per trasferire dati da un dispositivo.


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




