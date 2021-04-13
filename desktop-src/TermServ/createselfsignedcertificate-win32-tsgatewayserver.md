---
title: Metodo CreateSelfSignedCertificate della classe Win32_TSGatewayServer
description: Crea un certificato autofirmato e restituisce l'hash del certificato come \ 0034; out \ 0034; parametro.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CreateSelfSignedCertificate
- Metodo CreateSelfSignedCertificate Servizi Desktop remoto, classe Win32_TSGatewayServer
- Classe Win32_TSGatewayServer Servizi Desktop remoto, metodo CreateSelfSignedCertificate
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
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475640"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Metodo CreateSelfSignedCertificate della \_ classe TSGatewayServer Win32

Crea un certificato autofirmato e restituisce l'hash del certificato come parametro "out". Inoltre, aggiunge il testo " \_ \_ \_ certificato autofirmato del gateway di Servizi terminal \_ " alla proprietà di contesto del certificato, in modo che il certificato venga riconosciuto come certificato del Gateway Desktop remoto (Gateway Desktop remoto). Questo metodo usa un contenitore di chiavi specifico di Gateway Desktop remoto per creare il certificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SubjectName* \[ in\]
</dt> <dd>

Nome del soggetto del certificato autofirmato.

</dd> <dt>

*Certhash* \[ out\]
</dt> <dd>

Hash del certificato.

</dd> </dl>

## <a name="remarks"></a>Commenti

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

[**\_TSGatewayServer Win32**](win32-tsgatewayserver.md)
</dt> </dl>

 

