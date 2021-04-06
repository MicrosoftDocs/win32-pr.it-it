---
title: Metodo seservers della classe Win32_TSGatewayLoadBalancer
description: Imposta la proprietà Servers con l'elenco dei server di bilanciamento del carico di Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Metodo seservers Servizi Desktop remoto
- Metodo seservers Servizi Desktop remoto, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto, metodo seservers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d1123ce82844fb501f3562014b93337502b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742370"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Metodo seservers della classe Win32 \_ TSGatewayLoadBalancer

Imposta la proprietà **Servers** con l'elenco dei server di bilanciamento del carico di desktop remoto Gateway (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Server* \[ di in\]
</dt> <dd>

Elenco delimitato da punti e virgola di server di bilanciamento del carico di Gateway Desktop remoto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se più server si trovano nel parametro *Server* e uno dei server non può essere elaborato, nessuno dei server verrà elaborato.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

