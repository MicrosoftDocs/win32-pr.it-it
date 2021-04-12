---
title: Proprietà EnableCredSspSupport di IMsRdpClientAdvancedSettings6
description: Specifica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517757"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a>Proprietà IMsRdpClientAdvancedSettings6:: EnableCredSspSupport

Specifica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se CredSSP è abilitato per questa connessione. Impostare su **Variant \_ true** per abilitare CredSSP o **Variant \_ false** in caso contrario.

## <a name="remarks"></a>Commenti

Questa proprietà è supportata solo dai client Connessione Desktop remoto 6,1 e 7,0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





