---
title: Proprietà PublicMode IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per la modalità pubblica. La modalità pubblica impedisce al client di memorizzare nella cache i dati utente nel sistema locale.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- Proprietà PublicMode Servizi Desktop remoto
- Proprietà PublicMode Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto proprietà , PublicMode
- Proprietà PublicMode Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto proprietà , PublicMode
- Proprietà PublicMode Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto proprietà , PublicMode
- Proprietà PublicMode Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto proprietà , PublicMode
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
ms.openlocfilehash: 8f5577c01d50b9f7e82a7430d51631c90db7f83e32c0fd20273c524eecdecb26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001349"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a>Proprietà IMsRdpClientAdvancedSettings5::P ublicMode

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

Imposta l'impostazione della modalità pubblica **su VARIANT \_ TRUE** **o VARIANT \_ FALSE.** Se impostato su **VARIANT \_ TRUE,** l'impostazione della modalità pubblica è abilitata.

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

 

 





