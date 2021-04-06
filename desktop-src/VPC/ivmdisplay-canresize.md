---
title: Proprietà IVMDisplay CanResize (VPCCOMInterfaces. h)
description: Determina se il Guest consente le modifiche di risoluzione.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- Proprietà CanResize Virtual PC
- Proprietà CanResize Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà CanResize
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743471"
---
# <a name="ivmdisplaycanresize-property"></a>Proprietà IVMDisplay:: CanResize

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se il Guest consente le modifiche di risoluzione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a>Valore proprietà

**Variante \_ TRUE** se il Guest consente modifiche di risoluzione e **Variant \_ false** in caso contrario.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                                                                              |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **null**.<br/>                                                                                                                 |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>                    | La configurazione è sconosciuta.<br/>                                                                                                              |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>               | Per questa operazione è necessario che la macchina virtuale sia in esecuzione.<br/>                                                                                    |
| <dl> <dt>Macchina virtuale \_ E \_ Nessuna \_ visualizzazione</dt> <dt>0xA0040850</dt> </dl>                    | Non sono stati trovati dispositivi video per la macchina virtuale.<br/>                                                                                   |
| <dl> <dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt> </dl> | La funzionalità componenti di integrazione non è disponibile. i componenti di integrazione non sono installati o la funzionalità è stata disabilitata.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

