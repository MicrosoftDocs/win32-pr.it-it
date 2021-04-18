---
title: Proprietà PCB IMsRdpClientAdvancedSettings6
description: Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server. | Proprietà PCB IMsRdpClientAdvancedSettings6
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PCB
- Servizi Desktop remoto proprietà PCB, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PCB
- Servizi Desktop remoto proprietà PCB, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PCB
- Servizi Desktop remoto proprietà PCB, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PCB
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da9cfa12ec944ea8f745ec3399c2a53f6b7c6b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321187"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a>IMsRdpClientAdvancedSettings6::P la proprietà CB

Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a>Valore proprietà

Specifica l'impostazione del BLOB da usare prima della connessione.

## <a name="remarks"></a>Commenti

Questa proprietà è supportata solo dai client Connessione Desktop remoto 6,1 e 7,0.

Il server utilizza l'impostazione BLOB per identificare il processo di destinazione per la connessione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                |
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

 

 





