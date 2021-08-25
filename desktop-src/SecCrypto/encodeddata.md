---
description: Rappresenta un blocco di dati con codifica ASN.1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Oggetto EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ba17056aaf2b038abb519c1eff230f6cccb396edea1ee9c1f96077d572e63fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874861"
---
# <a name="encodeddata-object"></a>Oggetto EncodedData

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) nello spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto EncodedData** rappresenta un blocco di dati con codifica ASN.1.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto EncodedData** viene restituito da diverse proprietà dell'oggetto CAPICOM. Quando viene restituito, questo oggetto viene usato per eseguire le attività seguenti:

-   Ottenere una rappresentazione di stringa dei dati codificati.
-   Ottenere l'oggetto decodificatore, se esistente, associato ai dati codificati.
-   Determinare il tipo di dati codificati.

## <a name="members"></a>Membri

**L'oggetto EncodedData** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto EncodedData** dispone di questi metodi.



| Metodo                                 | Descrizione                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [**Decoder**](encodeddata-decoder.md) | Ottiene un oggetto decodificatore, se presente.<br/>             |
| [**Formato**](encodeddata-format.md)   | Restituisce una rappresentazione di stringa dei dati codificati.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto EncodedData** ha queste proprietà.



| Proprietà                                      | Tipo di accesso          | Descrizione                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [**Valore**](encodeddata-value.md)<br/> | Sola lettura<br/> | Recupera i dati codificati. Si tratta della proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

L'unico tipo supportato di dati codificati è [**CertificatePolicies.**](certificatepolicies.md)

Impossibile **creare l'oggetto EncodedData.**

Le proprietà dell'oggetto CAPICOM seguenti restituiscono un **oggetto EncodedData:**

-   **PublicKey.EncodedKey**
-   **PublicKey.EncodedParameters**
-   **Extension.EncodedData**
-   **Policy.EncodedData**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
