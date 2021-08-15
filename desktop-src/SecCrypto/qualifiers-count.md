---
description: Recupera il numero di oggetti Qualifier nella raccolta.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Proprietà Qualifiers.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fd4cfe0d600c99251db77b1764edb83353b01143fc5179c1efc29673e30e734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900947"
---
# <a name="qualifierscount-property"></a>Proprietà Qualifiers.Count

\[La **proprietà Count** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare L'OID per i criteri certificato per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione Criteri di certificato.\]

La **proprietà Count** recupera il numero di oggetti [**Qualifier**](qualifier.md) nella raccolta.

## <a name="syntax"></a>Sintassi


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di [**oggetti Qualifier**](qualifier.md) nella raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori**](qualifiers.md)
</dt> </dl>

 

 
