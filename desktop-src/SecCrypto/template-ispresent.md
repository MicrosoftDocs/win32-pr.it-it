---
description: Recupera un valore booleano che indica se l'estensione del modello è presente.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Proprietà Template. Presenter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324593"
---
# <a name="templateispresent-property"></a>Proprietà Template. Presenter

\[La proprietà **impresent** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]

La proprietà **impresent** recupera un valore booleano che indica se l'estensione del modello è presente.

## <a name="syntax"></a>Sintassi


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, è presente l'estensione del modello.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modello**](template.md)
</dt> </dl>

 

 
