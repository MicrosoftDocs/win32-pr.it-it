---
description: Rappresenta una raccolta di qualificatori.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Oggetto Qualifiers (IADs. h)
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
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326891"
---
# <a name="qualifiers-object"></a>Oggetto qualificatori

\[L'oggetto **qualificatori** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]

L'oggetto **Qualifiers** rappresenta una raccolta di qualificatori.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **qualificatori** viene utilizzato per eseguire le attività seguenti:

-   Recuperare una proprietà estesa specifica dalla raccolta.
-   Recuperare il numero di proprietà estese nella raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **qualificatori** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **qualificatori** ha queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](qualifiers-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](qualifiers-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di qualificatori nella raccolta.<br/>                                                                                                                                                                |
| [**Elemento**](qualifiers-item.md)<br/>         | Sola lettura<br/> | Recupera un oggetto [**qualificatore**](qualifier.md) che rappresenta il qualificatore indicizzato della raccolta. Si tratta della proprietà predefinita.<br/>                                                                             |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **qualificatori** .

La proprietà dell'oggetto [**PolicyInformation. Qualifiers**](policyinformation-qualifiers.md) CAPICOM restituisce un oggetto **qualificatori** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| Intestazione<br/>          | <dl> <dt>IADs. h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
