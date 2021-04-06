---
title: Metodo IVMKeyboard (VPCCOMInterfaces. h)
description: Determina se il tasto specificato è inattivo.
ms.assetid: 7541d678-762a-4c2e-80cd-686bb56c9cd7
keywords:
- Metodo di stampa Virtual PC
- Metodo di stampa Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo di stampa
topic_type:
- apiref
api_name:
- IVMKeyboard.IsPressed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a4185fa0310994bc1cffa917348dfca2fdedfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742599"
---
# <a name="ivmkeyboardispressed-method"></a>Metodo IVMKeyboard::

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se il tasto specificato è inattivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsPressed(
  [in]          BSTR         key,
  [out, retval] VARIANT_BOOL *pressed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Codice chiave per la chiave il cui stato deve essere sottoposto a query.

</dd> <dt>

con *pressione* \[ out, retval\]
</dt> <dd>

**True** se la chiave è attualmente premuta; in caso contrario, **false** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                   |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>         | Un parametro è **null**.<br/>                                        |
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

 

