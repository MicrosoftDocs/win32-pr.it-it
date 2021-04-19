---
description: Rappresenta una raccolta di oggetti certificate.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Oggetto Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323979"
---
# <a name="certificates-object"></a>Oggetto Certificates

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **Certificates** rappresenta una raccolta di oggetti [**Certificate**](certificate.md) . Ogni oggetto [**certificato**](certificate.md) rappresenta un singolo [*certificato digitale*](../secgloss/d-gly.md).

L'oggetto **Certificates** espone le interfacce seguenti:

-   **ICertificates2**: introdotta in capicol 2,0.
-   **ICertificates**: introdotta in capicol 1,0.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **certificati** viene utilizzato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un oggetto [**certificato**](certificate.md) da o verso la raccolta.
-   Generare un subset della raccolta cercando un set di certificati o visualizzando una finestra di dialogo per selezionare i certificati.
-   Cancellare tutti gli oggetti [**certificato**](certificate.md) dalla raccolta.
-   Recuperare il numero di certificati nella raccolta.
-   Recuperare un oggetto [**certificato**](certificate.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **certificati** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'oggetto **Certificates** .



| Metodo                                | Descrizione                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](certificates-add.md)       | Aggiunge un oggetto [**certificato**](certificate.md) alla raccolta.<br/> (Ereditato da **CertificatesICertificates2**)                                        |
| [**Deselezionare**](certificates-clear.md)   | Rimuove tutti gli oggetti [**certificato**](certificate.md) dalla raccolta.<br/> (Ereditato da **CertificatesICertificates2**)                                |
| [**Find**](certificates-find.md)     | Restituisce un oggetto **Certificates** che contiene tutti i certificati che corrispondono ai criteri di ricerca specificati.<br/> (Ereditato da **CertificatesICertificates2**) |
| [**Rimuovi**](certificates-remove.md) | Rimuove un singolo oggetto [**certificato**](certificate.md) dalla raccolta.<br/> (Ereditato da **CertificatesICertificates2**)                            |
| [**Salva**](certificates-save.md)     | Salva i certificati in un file specificato.<br/> (Ereditato da **CertificatesICertificates2**)                                                                |
| [**Select**](certificates-select.md) | Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati.<br/> (Ereditato da **CertificatesICertificates2**)  |



 

### <a name="properties"></a>Proprietà

L'oggetto **Certificates** dispone di queste proprietà.



| Proprietà                                             | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](certificates-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di oggetti [**certificato**](certificate.md) nell'insieme.<br/>                                                                                                                                |
| [**Elemento**](certificates-item.md)<br/>         | Sola lettura<br/> | Recupera un oggetto [**certificato**](certificate.md) che rappresenta il certificato indicizzato della raccolta. Si tratta della proprietà predefinita.<br/> (Ereditato da **CertificatesICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **certificati** ed è sicuro per lo scripting. Il ProgID per l'oggetto **certificati** è "CAPICOM. Certificati. 2 ".

**CAPICOM 1. *x*:** il ProgID per l'oggetto **certificati** è "CAPICOM. Certificates. 1 ".

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

 

 
