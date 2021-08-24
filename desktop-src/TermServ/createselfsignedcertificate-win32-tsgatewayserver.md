---
title: Metodo CreateSelfSignedCertificate della Win32_TSGatewayServer classe
description: Crea un certificato autofirmato e restituisce l'hash del certificato come \ 0034;out \ 0034; Parametro.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Metodo CreateSelfSignedCertificate Servizi Desktop remoto
- Metodo CreateSelfSignedCertificate Servizi Desktop remoto , Win32_TSGatewayServer classe
- Win32_TSGatewayServer classe Servizi Desktop remoto , metodo CreateSelfSignedCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200b08da8d5eea9f31405a357650384081c407df4eb76820cd47a111e6b66aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139054"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Metodo CreateSelfSignedCertificate della classe \_ Win32 TSGatewayServer

Crea un certificato autofirmato e restituisce l'hash del certificato come parametro "out". Aggiunge anche il testo "TS GATEWAY SELF SIGNED CERTIFICATE" alla proprietà del contesto del certificato in modo che il certificato sia riconosciuto come certificato di Gateway \_ \_ Desktop remoto \_ \_ (Gateway Desktop remoto). Questo metodo usa un contenitore di chiavi specifico di Gateway Desktop remoto per creare il certificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SubjectName* \[ Pollici\]
</dt> <dd>

Nome del soggetto del certificato autofirmato.

</dd> <dt>

*CertHash* \[ Cambio\]
</dt> <dd>

Hash del certificato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 

