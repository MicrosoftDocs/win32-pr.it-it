---
description: Recupera l'URI che punta a un'istruzione CPS (Certification Practice Statement) pubblicata dall'autorità di certificazione (CA).
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Proprietà Qualifier. CPSPointer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331420"
---
# <a name="qualifiercpspointer-property"></a>Proprietà Qualifier. CPSPointer

\[La proprietà **CPSPointer** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]

La proprietà **CPSPointer** recupera l'URI che punta a un'istruzione CPS (Certification Practice Statement) pubblicata dall'autorità di certificazione (CA).

## <a name="syntax"></a>Sintassi


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a>Valore proprietà

URI che punta a un CPS pubblicato dalla CA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
