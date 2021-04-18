---
title: Proprietà PublicMode di IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per la modalità pubblica. La modalità pubblica impedisce al client di memorizzare nella cache i dati utente nel sistema locale.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301304"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a>IMsRdpClientAdvancedSettings5::P proprietà ublicMode

Imposta o recupera la configurazione per la modalità pubblica. La modalità pubblica impedisce al client di memorizzare nella cache i dati utente nel sistema locale.

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

Imposta l'impostazione della modalità pubblica su **Variant \_ true** o **Variant \_ false**. Se impostato su **Variant \_ true**, l'impostazione della modalità pubblica è abilitata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





