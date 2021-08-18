---
description: Rappresenta una raccolta di oggetti Extension.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Oggetto Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e484de5b4266c5a2458d15365d44a3461a7d1d0589e22391b1afd66e437e02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006839"
---
# <a name="extensions-object"></a>Oggetto Extensions

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto Extensions** rappresenta una raccolta di [**oggetti Extension.**](extension.md) Ogni [**oggetto Extension**](extension.md) rappresenta una singola estensione di certificato.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto** Extensions viene usato per eseguire le attività seguenti:

-   Recuperare il numero di estensioni di certificato nella raccolta.
-   Recuperare un oggetto [**Extension**](extension.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto Extensions** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Extensions** ha queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](extensions-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di [**oggetti Extension**](extension.md) nella raccolta.<br/>                                                                                                                                    |
| [**Elemento**](extensions-item.md)<br/>         | Sola lettura<br/> | Recupera [**l'oggetto Extension**](extension.md) che rappresenta l'estensione del certificato indicizzata della raccolta. Questa è la proprietà predefinita.<br/>                                                               |



 

## <a name="remarks"></a>Commenti

**L'oggetto** Extensions viene restituito [**dal metodo Certificate.Extensions.**](certificate-extensions.md)

Impossibile **creare** l'oggetto Extensions.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
