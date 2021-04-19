---
description: Consente di accedere al contesto di un oggetto certificato CAPICOM X. 509v3. Questo contesto consente l'uso del certificato di CAPICOM in altre derivazioni di CryptoAPI.
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
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332691"
---
# <a name="icertcontext-interface"></a>Interfaccia ICertContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

L'interfaccia **ICertContext** consente di accedere al contesto di un oggetto [**certificato**](certificate.md) capicol X. 509v3. Questo contesto consente l'uso del certificato di CAPICOM in altre derivazioni di CryptoAPI.

## <a name="when-to-use"></a>Utilizzo

Usare questa interfaccia quando è necessario usare un oggetto [**certificato**](certificate.md) CAPICOM in un'altra derivazione di CryptoAPI.

## <a name="members"></a>Membri

L'interfaccia **ICertContext** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **ICertContext** dispone di questi metodi.



| Metodo                                          | Descrizione                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](icertcontext-freecontext.md) | Rilascia un \_ contesto PCCERT acquisito tramite la proprietà [**CertContext**](icertcontext-certcontext.md) .<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **ICertContext** ha queste proprietà.



| Proprietà                                                   | Tipo di accesso           | Descrizione                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**CertContext**](icertcontext-certcontext.md)<br/> | Lettura/Scrittura<br/> | Imposta o Recupera il \_ contesto PCCERT di un certificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




