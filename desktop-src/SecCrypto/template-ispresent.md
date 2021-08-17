---
description: Recupera un valore booleano che indica se l'estensione del modello è presente.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Template.IsPresent - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0492f6abccf2ade6e652dba2c4ea13d9bbfc28f1a3d3c34008eb3338ccb1e426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897396"
---
# <a name="templateispresent-property"></a>Template.IsPresent - proprietà

\[La **proprietà IsPresent** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per il modello di certificato per recuperare il modello di estensione del certificato.\]

La **proprietà IsPresent** recupera un valore booleano che indica se l'estensione del modello è presente.

## <a name="syntax"></a>Sintassi


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true,** l'estensione del modello è presente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modello**](template.md)
</dt> </dl>

 

 
