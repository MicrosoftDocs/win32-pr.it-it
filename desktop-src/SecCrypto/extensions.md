---
description: Rappresenta una raccolta di oggetti di estensione.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Oggetto Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329018"
---
# <a name="extensions-object"></a>Oggetto Extensions

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **Extensions** rappresenta una raccolta di oggetti di [**estensione**](extension.md) . Ogni oggetto [**estensione**](extension.md) rappresenta una singola estensione del certificato.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **Extensions** viene utilizzato per eseguire le attività seguenti:

-   Recuperare il numero di estensioni del certificato nella raccolta.
-   Recuperare un oggetto [**estensione**](extension.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **Extensions** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **Extensions** dispone di queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](extensions-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di oggetti di [**estensione**](extension.md) nella raccolta.<br/>                                                                                                                                    |
| [**Elemento**](extensions-item.md)<br/>         | Sola lettura<br/> | Recupera l'oggetto di [**estensione**](extension.md) che rappresenta l'estensione del certificato indicizzato della raccolta. Si tratta della proprietà predefinita.<br/>                                                               |



 

## <a name="remarks"></a>Commenti

L'oggetto **Extensions** viene restituito dal metodo [**Certificate. Extensions**](certificate-extensions.md) .

Impossibile creare l'oggetto **Extensions** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
