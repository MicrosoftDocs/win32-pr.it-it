---
description: Raccolta di oggetti PolicyInformation.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Oggetto CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327996"
---
# <a name="certificatepolicies-object"></a>Oggetto CertificatePolicies

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per recuperare i criteri del certificato.\]

L'oggetto **CertificatePolicies** rappresenta una raccolta di oggetti [**PolicyInformation**](policyinformation.md) . Ogni oggetto [**PolicyInformation**](policyinformation.md) rappresenta un singolo criterio di certificato.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **CertificatePolicies** viene usato per eseguire le attività seguenti:

-   Recuperare il numero di criteri certificati nella raccolta.
-   Recuperare un oggetto [**PolicyInformation**](policyinformation.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **CertificatePolicies** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **CertificatePolicies** dispone di queste proprietà.



| Proprietà                                                    | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](certificatepolicies-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di oggetti [**PolicyInformation**](policyinformation.md) nell'insieme.<br/>                                                                                                                    |
| [**Elemento**](certificatepolicies-item.md)<br/>         | Sola lettura<br/> | Recupera un oggetto [**PolicyInformation**](policyinformation.md) che rappresenta i criteri di certificato indicizzati della raccolta. Si tratta della proprietà predefinita.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **CertificatePolicies** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
