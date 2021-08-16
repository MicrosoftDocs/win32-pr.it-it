---
description: Rappresenta una raccolta di qualificatori.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Oggetto Qualifiers (Iads.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0f68dbeefefbe675199522dfbc5b1dab81b8a2840fa8b7d5189c72b811fcba7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900957"
---
# <a name="qualifiers-object"></a>Oggetto Qualifiers

\[**L'oggetto Qualifiers** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la classe [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri certificato per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione Criteri certificato.\]

**L'oggetto Qualifiers** rappresenta una raccolta di qualificatori.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto Qualifiers** viene usato per eseguire le attività seguenti:

-   Recuperare una proprietà estesa specifica dalla raccolta.
-   Recuperare il numero di proprietà estese nella raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto Qualifiers** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Qualifiers** ha queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](qualifiers-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](qualifiers-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di qualificatori nella raccolta.<br/>                                                                                                                                                                |
| [**Elemento**](qualifiers-item.md)<br/>         | Sola lettura<br/> | Recupera un oggetto [**Qualifier**](qualifier.md) che rappresenta il qualificatore indicizzato della raccolta. Si tratta della proprietà predefinita.<br/>                                                                             |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto** Qualifiers.

La proprietà dell'oggetto CAPICOM [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) restituisce un **oggetto Qualifiers.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| Intestazione<br/>          | <dl> <dt>Iads.h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
