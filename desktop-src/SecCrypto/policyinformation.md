---
description: Consente di accedere alle informazioni sui criteri di un'estensione.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Oggetto PolicyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324839"
---
# <a name="policyinformation-object"></a>Oggetto PolicyInformation

\[L'oggetto **PolicyInformation** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per elaborare le informazioni sui criteri nell'estensione criteri di certificato.\]

L'oggetto **PolicyInformation** fornisce l'accesso alle informazioni sui criteri di un'estensione.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **PolicyInformation** viene usato per eseguire le attività seguenti:

-   Recuperare l'OID del criterio.
-   Recuperare una raccolta dei qualificatori del criterio.

## <a name="members"></a>Membri

L'oggetto **PolicyInformation** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **PolicyInformation** dispone di queste proprietà.



| Proprietà                                                      | Descrizione                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**OID**](policyinformation-oid.md)<br/>               | Recupera l'OID del criterio come oggetto [**OID**](oid.md) . Si tratta della proprietà predefinita.<br/>       |
| [**Qualificatori**](policyinformation-qualifiers.md)<br/> | Recupera una raccolta dei qualificatori del criterio come oggetto [**qualificatori**](qualifiers.md) .<br/> |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **PolicyInformation** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
