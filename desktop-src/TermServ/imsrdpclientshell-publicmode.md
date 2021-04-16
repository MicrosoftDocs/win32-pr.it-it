---
title: Proprietà PublicMode di IMsRdpClientShell
description: Specifica o recupera se la modalità pubblica è abilitata.
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientShell
- Interfaccia IMsRdpClientShell Servizi Desktop remoto, proprietà PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4129b3a9eeb62af0fa6e970c812ea6adf9670c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477759"
---
# <a name="imsrdpclientshellpublicmode-property"></a>IMsRdpClientShell::P proprietà ublicMode

Specifica o recupera se la modalità pubblica è abilitata.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se la modalità pubblica è abilitata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell è definito come d012ae6d-c19a-4bfe-B367-201f8911f134<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





