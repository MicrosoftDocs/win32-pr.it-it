---
title: Proprietà IMsRdpClientNonScriptable3 NegotiateSecurityLayer
description: Specifica o recupera un valore che indica se il livello di sicurezza della negoziazione è abilitato per la connessione.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto proprietà , NegotiateSecurityLayer
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto proprietà , NegotiateSecurityLayer
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto proprietà , NegotiateSecurityLayer
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto , oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto proprietà , NegotiateSecurityLayer
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto , oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto proprietà , NegotiateSecurityLayer
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto , oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto proprietà , NegotiateSecurityLayer
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto , oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto proprietà , NegotiateSecurityLayer
- Proprietà NegotiateSecurityLayer Servizi Desktop remoto, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto proprietà , NegotiateSecurityLayer
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
ms.openlocfilehash: 13f87abb5323289e60e3d29fa93d5e858a9a755224e7161ba28970ef5ccb186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771551"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>Proprietà IMsRdpClientNonScriptable3::NegotiateSecurityLayer

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

Se questa proprietà è impostata su **VARIANT \_ FALSE** e l'Autenticazione a livello di rete (NLA) è abilitato nel sistema operativo client, il client non negozierà il livello di sicurezza e userà l'autenticazione a livello di rete per proteggere la connessione RDP. Se questa proprietà è impostata su **VARIANT \_ TRUE,** il client negozierà tra l'autenticazione a livello di rete e la sicurezza RDP di base.

> [!Note]  
> La disabilitazione della negoziazione del livello di sicurezza è possibile solo quando ci si connette a un server Host sessione Desktop remoto (Host sessione Desktop remoto) che esegue Windows Vista o sistemi operativi successivi. Se questa proprietà è abilitata e il client tenta di connettersi a un server Host sessione Desktop remoto che esegue un sistema operativo precedente, la connessione avrà esito negativo.

 

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

 

 





