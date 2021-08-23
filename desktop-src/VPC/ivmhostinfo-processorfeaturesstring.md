---
title: Proprietà IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 1040702df250c906bb32af5068a340c37a9ba3faabee3af17d8397bfdc8059e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998891"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>Proprietà IVMHostInfo::P rocessorFeaturesString

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera le funzionalità dell'elenco supportate dal processore host.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>Valore proprietà

Elenco delimitato da virgole di funzionalità. Un esempio è "MMX,SSE,SSE2,x86-64".



| Valore                                                                                 | Significato                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>"AMD-V"</dt> </dl>    | Supporta le estensioni AMD Virtualization.<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | Supporta le estensioni intel virtualization technology.<br/> |
| <dl> <dt>"HAVD"</dt> </dl>     | La virtualizzazione assistita dall'hardware è disabilitata.<br/>            |
| <dl> <dt>"HAVE"</dt> </dl>     | La virtualizzazione assistita dall'hardware è abilitata.<br/>             |
| <dl> <dt>"MMX"</dt> </dl>      | Supporta le estensioni MMX.<br/>                             |
| <dl> <dt>"SSE"</dt> </dl>      | Supporta l'Streaming SIMD Extensions.<br/>                  |
| <dl> <dt>"SSE2"</dt> </dl>     | Supporta l'Streaming SIMD Extensions 2.<br/>                |
| <dl> <dt>"SSE3"</dt> </dl>     | Supporta l'Streaming SIMD Extensions 3.<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | Supporta le estensioni Trusted Execution Technology.<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | Supporta le estensioni x86-64.<br/>                              |



 

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo è definito come \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

