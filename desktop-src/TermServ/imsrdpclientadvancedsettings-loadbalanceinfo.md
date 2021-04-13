---
title: Proprietà LoadBalanceInfo di IMsRdpClientAdvancedSettings
description: Specifica il cookie di bilanciamento del carico che verrà inserito nel pacchetto della richiesta di connessione X. 224 nella sequenza di connessione del protocollo server host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà LoadBalanceInfo
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400449"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a>Proprietà IMsRdpClientAdvancedSettings:: LoadBalanceInfo

Specifica il cookie di bilanciamento del carico che verrà inserito nel pacchetto della richiesta di connessione X. 224 nella sequenza di connessione del protocollo server host sessione Desktop remoto (host sessione Desktop remoto).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore al nuovo cookie. Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Le informazioni sul bilanciamento del carico vengono utilizzate dai router di bilanciamento del carico per scegliere il server migliore per il client quando si utilizzano farm di server Host sessione Desktop remoto. Il server Host sessione Desktop remoto non utilizza queste informazioni e lo eliminerà.

Il cookie utilizza la sintassi seguente, con distinzione tra maiuscole e minuscole:

**Cookie: MSTS =**_IpAddressAndPortNumber_*_\\ r \\ n_*

Dove *IpAddressAndPortNumber* è l'indirizzo IP e il numero di porta, in ordine byte di rete.

Ad esempio, il cookie usato per accedere all'indirizzo IP di 172.31.249.216, il numero di porta 3389 è il seguente:

**Cookie: MSTS = 3640205228.15629.0000 \\ r \\ n**

I quattro zeri finali sono facoltativi e sono riservati. Il separatore decimale finale è obbligatorio, così come il ritorno a capo e il avanzamento riga finali. La lunghezza della stringa, in caratteri, deve essere un multiplo pari a 2, quindi aggiungere uno spazio se necessario.

Se non viene fornito alcun cookie, il valore predefinito è **cookie: mstshash =**_username_*_\\ r \\ n_*.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                        |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                  |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





