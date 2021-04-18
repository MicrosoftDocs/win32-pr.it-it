---
title: Proprietà NegotiateSecurityLayer di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se il livello di sicurezza della negoziazione è abilitato per la connessione.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301628"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>Proprietà IMsRdpClientNonScriptable3:: NegotiateSecurityLayer

Specifica o recupera un valore che indica se il livello di sicurezza della negoziazione è abilitato per la connessione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se abilitare la negoziazione del livello di sicurezza.

## <a name="remarks"></a>Commenti

Se questa proprietà è impostata su **Variant \_ FALSE** e autenticazione a livello di rete (NLA) è abilitata nel sistema operativo client, il client non negozierà il livello di sicurezza e utilizzerà invece NLA per proteggere la connessione RDP. Se questa proprietà è impostata su **Variant \_ true**, il client effettuerà la negoziazione tra NLA e la sicurezza RDP di base.

> [!Note]  
> La disabilitazione della negoziazione del livello di sicurezza è possibile solo quando ci si connette a un server di host sessione Desktop remoto (host sessione Desktop remoto) che esegue Windows Vista o sistemi operativi successivi. Se questa proprietà è abilitata e il client tenta di connettersi a un server Host sessione Desktop remoto che esegue un sistema operativo precedente, la connessione avrà esito negativo.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





