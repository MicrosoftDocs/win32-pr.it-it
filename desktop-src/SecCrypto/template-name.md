---
description: Recupera il nome del modello.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Proprietà Template.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330600"
---
# <a name="templatename-property"></a>Proprietà Template.Name

\[La proprietà **Name** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]

La proprietà **Name** Recupera il nome del modello.

## <a name="syntax"></a>Sintassi


```VB
Template.Name As String
```



## <a name="property-value"></a>Valore proprietà

Nome del modello.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modello**](template.md)
</dt> </dl>

 

 
