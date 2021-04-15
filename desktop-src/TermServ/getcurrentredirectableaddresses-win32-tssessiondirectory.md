---
title: Metodo GetCurrentRedirectableAddresses della classe Win32_TSSessionDirectory
description: Ottiene l'elenco attualmente configurato degli indirizzi idonei DNS che possono essere usati per il reindirizzamento.
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetCurrentRedirectableAddresses
- Metodo GetCurrentRedirectableAddresses Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo GetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b4a859c77f449fb5a8f436be6e18c058ca59f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478893"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Metodo GetCurrentRedirectableAddresses della \_ classe TSSessionDirectory Win32

Ottiene l'elenco attualmente configurato degli indirizzi idonei DNS che possono essere usati per il reindirizzamento.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTokenRedirection* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Flag che indica se deve essere utilizzato il reindirizzamento del token.

</dd> <dt>

*IPAddress* \[ out\]
</dt> <dd>

Tipo: **stringa \[ \]**

Una matrice degli indirizzi IP idonei DNS attualmente configurati che possono essere usati per il reindirizzamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

