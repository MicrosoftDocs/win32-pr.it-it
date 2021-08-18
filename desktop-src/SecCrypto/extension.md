---
description: Rappresenta una singola estensione del certificato.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Oggetto estensione (Mmcobj.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e311c6dc69f40d32163c70cabf6a38780a989764bd77f4023c61ede5c1ba713c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006959"
---
# <a name="extension-object"></a>Oggetto estensione

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto Extension** rappresenta una singola estensione del certificato.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto** Extension viene usato per eseguire le attività seguenti:

-   Recuperare l'OID dell'estensione del certificato.
-   Recuperare i dati dell'estensione del certificato rappresentati da un [**oggetto EncodedData.**](encodeddata.md)
-   Determinare se l'estensione del certificato è contrassegnata come critica.

## <a name="members"></a>Membri

**L'oggetto Extension** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Extension** ha queste proprietà.



| Proprietà                                                | Tipo di accesso          | Descrizione                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**EncodedData**](extension-encodeddata.md)<br/> | Sola lettura<br/> | Recupera i dati codificati per l'estensione.<br/>                                      |
| [**IsCritical**](extension-iscritical.md)<br/>   | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione è contrassegnata come critica.<br/> |
| [**Oid**](extension-oid.md)<br/>                 | Sola lettura<br/> | Recupera l'identificatore di oggetto per l'estensione. Si tratta della proprietà predefinita.<br/>   |



 

## <a name="remarks"></a>Commenti

Impossibile **creare** l'oggetto Extension.

**L'oggetto Extension** viene usato dall'oggetto [**raccolta**](extensions.md) Extensions.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| Intestazione<br/>                | <dl> <dt>Mmcobj.h</dt> </dl>    |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
