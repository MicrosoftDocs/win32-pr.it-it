---
description: Fornisce l'accesso al contesto di un oggetto certificato CAPICOM X.509v3. Questo contesto consente l'uso del certificato CAPICOM in altre derivazioni di CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Interfaccia ICertContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 693e259c730209049f669d1499001d026b3d11088c7bef09616826a4673cac0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006039"
---
# <a name="icertcontext-interface"></a>Interfaccia ICertContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

**L'interfaccia ICertContext** fornisce l'accesso al contesto di un oggetto Certificato CAPICOM X.509v3. [](certificate.md) Questo contesto consente l'uso del certificato CAPICOM in altre derivazioni di CryptoAPI.

## <a name="when-to-use"></a>Utilizzo

Usare questa interfaccia quando è necessario usare un oggetto Certificato [**CAPICOM**](certificate.md) in un'altra derivazione di CryptoAPI.

## <a name="members"></a>Membri

**L'interfaccia ICertContext** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia ICertContext** include questi metodi.



| Metodo                                          | Descrizione                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](icertcontext-freecontext.md) | Rilascia un OGGETTO PCCERT \_ CONTEXT acquisito tramite la proprietà [**CertContext.**](icertcontext-certcontext.md)<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia ICertContext** ha queste proprietà.



| Proprietà                                                   | Tipo di accesso           | Descrizione                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**CertContext**](icertcontext-certcontext.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera il CONTESTO PCCERT \_ di un certificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




