---
description: Recupera il nome dell'organizzazione associata al qualificatore.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Proprietà Qualifier. OrganizationName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329009"
---
# <a name="qualifierorganizationname-property"></a>Proprietà Qualifier. OrganizationName

\[La proprietà **OrganizationName** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]

La proprietà **OrganizationName** Recupera il nome dell'organizzazione associata al qualificatore. Questa proprietà può essere vuota.

## <a name="syntax"></a>Sintassi


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a>Valore proprietà

Nome dell'organizzazione associata al qualificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
