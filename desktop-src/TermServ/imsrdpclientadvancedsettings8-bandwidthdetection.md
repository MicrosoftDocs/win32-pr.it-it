---
title: Proprietà BandwidthDetection di IMsRdpClientAdvancedSettings8
description: Specifica se le modifiche della larghezza di banda vengono rilevate automaticamente.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BandwidthDetection
- Servizi Desktop remoto proprietà BandwidthDetection, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BandwidthDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301222"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a>Proprietà IMsRdpClientAdvancedSettings8:: BandwidthDetection

Specifica se le modifiche della larghezza di banda vengono rilevate automaticamente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a>Valore proprietà

**Variante \_ TRUE** se le modifiche della larghezza di banda vengono rilevate automaticamente o **Variant \_ false** in alternativa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





