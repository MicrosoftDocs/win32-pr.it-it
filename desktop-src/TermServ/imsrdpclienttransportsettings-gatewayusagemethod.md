---
title: Proprietà GatewayUsageMethod di IMsRdpClientTransportSettings
description: Specifica quando utilizzare un server Gateway Desktop remoto di Desktop remoto.
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayUsageMethod
- Servizi Desktop remoto proprietà GatewayUsageMethod, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301217"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>Proprietà IMsRdpClientTransportSettings:: GatewayUsageMethod

Specifica quando utilizzare un server Gateway Desktop remoto di Desktop remoto.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a>Valore proprietà

Variabile **ULONG** che specifica il metodo di utilizzo del server Gateway Desktop remoto. Questo parametro può avere uno dei valori seguenti.

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ \_Modalità proxy \_ Nessuna \_ diretta** (0 (0x0))


</dt> <dd>

Non usare un server Gateway Desktop remoto. Nell'interfaccia utente del client Connessione Desktop remoto (RDC), la casella **di controllo Ignora server Gateway Desktop remoto per indirizzi locali** è deselezionata.

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ \_Modalità proxy \_ diretta** (1 (0x1))


</dt> <dd>

Usare sempre un server Gateway Desktop remoto. Nell'interfaccia utente del client RDC, la casella **di controllo Ignora server Gateway Desktop remoto per indirizzi locali** è deselezionata.

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ \_ \_ Rilevamento modalità proxy** (2 (0x2))


</dt> <dd>

Utilizzare un server Gateway Desktop remoto se non è possibile effettuare una connessione diretta al server Host sessione Desktop remoto. Nell'interfaccia utente del client RDC è selezionata la casella **di controllo Ignora server Gateway Desktop remoto per indirizzi locali** .

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ \_ \_ Impostazione predefinita modalità proxy** (3 (0x3))


</dt> <dd>

Utilizzare le impostazioni predefinite del server Gateway Desktop remoto.

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ \_ \_ \_ Rilevamento nessuna modalità proxy** (4 (0x4))


</dt> <dd>

Non usare un server Gateway Desktop remoto. Nell'interfaccia utente del client RDC è selezionata la casella **di controllo Ignora server Gateway Desktop remoto per indirizzi locali** .

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





