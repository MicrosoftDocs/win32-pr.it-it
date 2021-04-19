---
description: Fornisce accesso in sola lettura alle proprietà dell'utilizzo chiavi avanzato (EKU) di un certificato.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Oggetto ExtendedKeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330133"
---
# <a name="extendedkeyusage-object"></a>Oggetto ExtendedKeyUsage

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **ExtendedKeyUsage** fornisce accesso in sola lettura alle proprietà di utilizzo chiavi avanzato (EKU) di un certificato.

## <a name="members"></a>Membri

L'oggetto **ExtendedKeyUsage** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **ExtendedKeyUsage** dispone di queste proprietà.



| Proprietà                                                     | Tipo di accesso          | Descrizione                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EKU**](extendedkeyusage-ekus.md)<br/>             | Sola lettura<br/> | Raccolta [**EKU**](ekus.md) che contiene gli oggetti [**EKU**](eku.md) per il certificato.<br/>                            |
| [**IsCritical**](extendedkeyusage-iscritical.md)<br/> | Sola lettura<br/> | Recupera un valore **booleano** che indica se l'estensione EKU è contrassegnata come critica.<br/>                                   |
| [**IsPresent**](extendedkeyusage-ispresent.md)<br/>   | Sola lettura<br/> | Recupera un valore **booleano** che indica se l'estensione EKU è presente.<br/> Si tratta della proprietà predefinita. <br/> |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **ExtendedKeyUsage** .

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

 

 
