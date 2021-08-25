---
title: AccessPermission
description: Descrive l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe. Questo ACL viene usato solo dalle applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Valore del Registro di sistema AccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641512d34b963879ceb3d1a6266a017836879b224b228edb3ad62d61300fb03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551345"
---
# <a name="accesspermission"></a>AccessPermission

Descrive l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe. Questo ACL viene usato solo dalle applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore REG \_ BINARY.** Contiene dati che descrivono l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe. Quando si riceve una richiesta di connessione a un oggetto esistente di questa classe, l'ACL viene controllato dall'applicazione chiamata durante la rappresentazione del chiamante. Se il controllo di accesso ha esito negativo, la connessione non è consentita. Se questo valore denominato non esiste, viene testato [**l'ACL DefaultAccessPermission**](defaultaccesspermission.md) per determinare se la connessione deve essere consentita.

Per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o non usano l'interfaccia [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) per specificare l'AppID, il file eseguibile del file binario dell'applicazione deve essere mappato all'AppID dell'applicazione come descritto in [**AppID**](appid.md). Questa operazione è necessaria in modo che COM possa individuare l'AppID dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Coinitializesecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 