---
description: Recupera il contenuto dell'avviso dell'utente.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Proprietà Qualifier.ExplicitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 60753e0e7fa9996f9584070d6fac2d12d3a483b681fa61b72cf2e59cc2898995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901112"
---
# <a name="qualifierexplicittext-property"></a>Proprietà Qualifier.ExplicitText

\[La **proprietà ExplicitText** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare L'OID per i criteri certificato per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione Criteri di certificato.\]

La **proprietà ExplicitText** recupera il contenuto dell'avviso utente. Questa proprietà può essere vuota.

## <a name="syntax"></a>Sintassi


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a>Valore proprietà

Contenuto dell'avviso dell'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
