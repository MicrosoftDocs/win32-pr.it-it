---
description: Rappresenta una catena di certificati attendibili.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chain (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326769"
---
# <a name="chain-object"></a>Chain (oggetto)

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **Chain** rappresenta una catena di certificati attendibili.

Questo oggetto fornisce proprietà e metodi per compilare una catena di certificati attendibili per verificare la validità dei certificati. La catena viene compilata usando il valore della proprietà [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) e le impostazioni dei criteri di un oggetto [**CertificateStatus**](certificatestatus.md) .

L'oggetto **Chain** espone le interfacce seguenti:

-   **IChain2**: introdotta in capicol 2,0.
-   **IChain**: introdotta in capicol 1,0.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **Chain** viene utilizzato per eseguire le attività seguenti:

-   Compilare una catena di certificati.
-   Ottenere il OID di tutti i criteri del certificato e dell'applicazione validi per la catena.
-   Verificare lo stato dei certificati nella catena.
-   Ottenere informazioni estese sull'errore.
-   Recuperare la raccolta di certificati nella catena.

## <a name="members"></a>Membri

L'oggetto **Chain** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Chain** presenta questi metodi.



| Metodo                                                   | Descrizione                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](chain-applicationpolicies.md) | Restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri dell'applicazione OID validi per la catena.<br/> (Ereditato da **ChainIChain2**)                                                                                                                                                          |
| [**Compilazione**](chain-build.md)                             | Compila una catena di verifica dei certificati da un certificato finale al [*certificato radice*](../secgloss/r-gly.md)attendibile, restituendo un valore booleano che indica la validità complessiva della catena.<br/> (Ereditato da **ChainIChain2IChain**) |
| [**CertificatePolicies**](chain-certificatepolicies.md) | Restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri di certificato OID validi per la catena.<br/> (Ereditato da **ChainIChain2**)                                                                                                                                                          |
| [**ExtendedErrorInfo**](chain-extendederrorinfo.md)     | Restituisce una stringa che contiene informazioni aggiuntive sull'errore relative alla voce indicizzata.<br/> (Ereditato da **ChainIChain2**)                                                                                                                                                                                 |



 

### <a name="properties"></a>Proprietà

L'oggetto **Chain** dispone di queste proprietà.



| Proprietà                                              | Tipo di accesso          | Descrizione                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificati**](chain-certificates.md)<br/> | Sola lettura<br/> | Recupera una raccolta di [**certificati**](certificates.md) che rappresenta i certificati nella catena. Si tratta della proprietà predefinita.<br/> (Ereditato da **ChainIChain2IChain**) |
| [**Stato**](chain-status.md)<br/>             | Sola lettura<br/> | Recupera lo stato di validità della catena o di un certificato specifico nella catena.<br/> (Ereditato da **ChainIChain2IChain**)                                                       |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **Chain** ed è sicuro per lo scripting. Il ProgID per l'oggetto **Chain** è "CAPICOM. Chain. 2 ".

**CAPICOM 1. *x*:** il ProgID per l'oggetto **Chain** è capicom. Chain. 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
