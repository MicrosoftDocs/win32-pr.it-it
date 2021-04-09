---
title: Metodo IVMKeyboard pulsanteper (VPCCOMInterfaces. h)
description: Simula un tasto premuto.
ms.assetid: d945128a-ffde-465c-b615-83a1d5dc789f
keywords:
- Metodo pulsanteper Virtual PC
- Metodo pulsanteper Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo pulsanteper
topic_type:
- apiref
api_name:
- IVMKeyboard.PressKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8175447a819afa7f761899a7e0dd3cbbcc780631
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048496"
---
# <a name="ivmkeyboardpresskey-method"></a>IVMKeyboard::P metodo ressKey

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula un tasto premuto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PressKey(
  [in] BSTR key
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Codice chiave per la chiave da premere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                   |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>                                      |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>      | La stringa specificata è vuota o contiene un codice chiave non valido.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

