---
title: AccessPermission
description: Descrive l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe. Questo ACL viene usato solo da applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Valore AccessPermission del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474302"
---
# <a name="accesspermission"></a>AccessPermission

Descrive l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe. Questo ACL viene usato solo da applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **\_ binario REG** . Contiene dati che descrivono l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe. Quando riceve una richiesta di connessione a un oggetto esistente di questa classe, l'ACL viene controllato dall'applicazione chiamata durante la rappresentazione del chiamante. Se la verifica dell'accesso ha esito negativo, la connessione non è consentita. Se questo valore denominato non esiste, viene testato l'ACL [**DefaultAccessPermission**](defaultaccesspermission.md) per determinare se la connessione deve essere consentita.

Per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o non usano l'interfaccia [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) per specificare l'AppID, l'eseguibile del file binario dell'applicazione deve essere mappato all'AppID dell'applicazione come descritto in [**AppID**](appid.md). Questa operazione è necessaria affinché COM possa individuare l'AppID dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 