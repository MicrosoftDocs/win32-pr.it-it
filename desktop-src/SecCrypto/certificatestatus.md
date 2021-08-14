---
description: Contiene informazioni su come costruire una catena di certificati di attendibilità.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Oggetto CertificateStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c0c228a06da9d0a4dd93491908af0c0a2d0693125be57b675ca64e10378f253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770000"
---
# <a name="certificatestatus-object"></a>Oggetto CertificateStatus

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto CertificateStatus** contiene informazioni su come costruire una catena di certificati di attendibilità.

## <a name="members"></a>Membri

**L'oggetto CertificateStatus** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto CertificateStatus** dispone di questi metodi.



| Metodo                                                               | Descrizione                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](certificatestatus-applicationpolicies.md) | Restituisce una [**raccolta di OID**](oids.md) che rappresenta gli OID dei criteri dell'applicazione.<br/>                                           |
| [**CertificatePolicies**](certificatestatus-certificatepolicies.md) | Restituisce una [**raccolta di OID**](oids.md) che rappresenta gli OID dei criteri del certificato utilizzati durante la compilazione della catena.<br/>                |
| [**EKU**](certificatestatus-eku.md)                                 | Restituisce [**l'oggetto EKU**](eku.md) utilizzato per impostare gli elementi EKU da controllare per stabilire lo stato di validità di un certificato.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto CertificateStatus** ha queste proprietà.



| Proprietà                                                                        | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificati**](certificatestatus-certificates.md)<br/>               | Lettura/Scrittura<br/> | Imposta o recupera la raccolta di certificati che possono essere usati per compilare la catena di certificati.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** La [**proprietà Certificates**](certificatestatus-certificates.md) non è supportata.<br/>                    |
| [**CheckFlag**](certificatestatus-checkflag.md)<br/>                     | Lettura/Scrittura<br/> | Flag di controllo di validità. I valori possono essere uniti usando un **operatore OR** logico. Il flag di controllo predefinito è [**CAPICOM \_ CHECK ONLINE \_ \_ ALL.**](capicom-check-flag.md)<br/>                                                                                     |
| [**Risultato**](certificatestatus-result.md)<br/>                           | Sola lettura<br/>  | Indica se il certificato è valido. La validità del certificato viene verificata usando l'impostazione corrente della [**proprietà CheckFlag**](certificatestatus-checkflag.md) e le impostazioni dei criteri del certificato. Si tratta della proprietà predefinita.<br/> |
| [**UrlRetrievalTimeout**](certificatestatus-urlretrievaltimeout.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera l'intervallo di tempo prima che un URL venga determinato come non raggiungibile.<br/>                                                                                                                                                                     |
| [**VerificationTime**](certificatestatus-verificationtime.md)<br/>       | Lettura/Scrittura<br/> | Imposta o recupera l'ora di verifica del certificato.<br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto CertificateStatus.**

**L'oggetto CertificateStatus** viene restituito dal [**metodo Certificate.IsValid.**](certificate-isvalid.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**Catena**](chain.md)
</dt> </dl>

 

 
