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
ms.openlocfilehash: 8da0ad9681f3dd87227a7fe0b5a5419ceac4c7ee354fb1548427c100561e816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770840"
---
# <a name="certificatepolicies-object"></a>Oggetto CertificatePolicies

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la classe [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri certificato per recuperare i criteri del certificato.\]

**L'oggetto CertificatePolicies** rappresenta una raccolta di [**oggetti PolicyInformation.**](policyinformation.md) Ogni [**oggetto PolicyInformation**](policyinformation.md) rappresenta un singolo criterio certificato.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto CertificatePolicies** viene usato per eseguire le attività seguenti:

-   Recuperare il numero di criteri certificato nella raccolta.
-   Recuperare un oggetto [**PolicyInformation**](policyinformation.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto CertificatePolicies** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto CertificatePolicies** ha queste proprietà.



| Proprietà                                                    | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](certificatepolicies-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di [**oggetti PolicyInformation**](policyinformation.md) nella raccolta.<br/>                                                                                                                    |
| [**Elemento**](certificatepolicies-item.md)<br/>         | Sola lettura<br/> | Recupera un oggetto [**PolicyInformation**](policyinformation.md) che rappresenta i criteri del certificato indicizzato della raccolta. Si tratta della proprietà predefinita.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto CertificatePolicies.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
