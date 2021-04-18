---
title: Proprietà IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces. h)
description: Recupera le funzionalità dell'elenco supportate dal processore host.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Proprietà ProcessorFeaturesString Virtual PC
- Proprietà ProcessorFeaturesString Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà ProcessorFeaturesString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300930"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>IVMHostInfo::P proprietà rocessorFeaturesString

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera le funzionalità dell'elenco supportate dal processore host.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>Valore proprietà

Elenco delimitato da virgole di funzionalità. Un esempio è "MMX, SSE, SSE2, x86-64".



| Valore                                                                                 | Significato                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>"AMD-V"</dt> </dl>    | Supporta le estensioni di virtualizzazione AMD.<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | Supporta le estensioni della tecnologia di virtualizzazione Intel.<br/> |
| <dl> <dt>HAVD</dt> </dl>     | La virtualizzazione assistita mediante hardware è disabilitata.<br/>            |
| <dl> <dt>AVERE</dt> </dl>     | La virtualizzazione assistita mediante hardware è abilitata.<br/>             |
| <dl> <dt>MMX</dt> </dl>      | Supporta le estensioni MMX.<br/>                             |
| <dl> <dt>SSE</dt> </dl>      | Supporta il Streaming SIMD Extensions.<br/>                  |
| <dl> <dt>SSE2</dt> </dl>     | Supporta il Streaming SIMD Extensions 2.<br/>                |
| <dl> <dt>SSE3</dt> </dl>     | Supporta il Streaming SIMD Extensions 3.<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | Supporta le estensioni della tecnologia di esecuzione attendibile.<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | Supporta le estensioni x86-64.<br/>                              |



 

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>        |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

