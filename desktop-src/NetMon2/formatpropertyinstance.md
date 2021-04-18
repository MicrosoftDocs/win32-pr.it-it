---
description: Formatta i dati dell'istanza della proprietà utilizzando il formattatore generico fornito da Network Monitor.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Funzione FormatPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305928"
---
# <a name="formatpropertyinstance-function"></a>FormatPropertyInstance (funzione)

La funzione **FormatPropertyInstance** formatta i dati dell'istanza della proprietà utilizzando il formattatore generico fornito da Network Monitor.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpPropertyInst* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [PROPERTYINST](propertyinst.md) che contiene i dati dell'istanza.

In input il formattatore generico accetta i dati dell'istanza da uno dei membri di Unione **PROPERTYINST** e li converte in una stringa formattata predefinita.

Nell'output il formattatore generico imposta il membro **szPropertyText** della struttura **PROPERTYINST** su un puntatore alla stringa formattata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di NMerr. h.

## <a name="remarks"></a>Commenti

La DLL del parser chiama indirettamente la funzione **FormatPropertyInstance** quando il formattatore generico è necessario per formattare i dati per la visualizzazione nel riquadro dei dettagli dell'interfaccia utente di Network Monitor. Per chiamare **FormatPropertyInstance** , specificarlo nel membro **InstanceData** della struttura [PROPERTYINFO](propertyinfo.md) quando si definisce la proprietà.

> [!Note]  
> Il parser non riconosce la funzione chiamata quando deve formattare un'istanza di una proprietà. La funzione può essere **FormatPropertyInstance** o una funzione di formato personalizzata definita dal parser. Il parser chiama qualsiasi funzione format specificata dal membro **InstanceData** della struttura **PROPERTYINFO** per la proprietà.

 

Per ulteriori informazioni e un esempio di come implementare [formatproperties](formatproperties.md), vedere [implementazione di formatproperties](implementing-formatproperties.md). Per altre informazioni su come il formattatore generico formatta tipi diversi di dati, vedere [output del formattatore generico](generic-formatter-output.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




