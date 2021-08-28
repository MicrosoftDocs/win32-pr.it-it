---
description: 'Oggetto Certificates: rappresenta una raccolta di oggetti Certificate.'
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
ms.openlocfilehash: 4ccd66085f96ac7f3567ca3bf993d7d31c9bc70437199701fe88165adf52d03e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126721"
---
# <a name="certificates-object"></a>Oggetto Certificates

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto Certificates** rappresenta una raccolta di [**oggetti**](certificate.md) Certificate. Ogni [**oggetto Certificate**](certificate.md) rappresenta un singolo certificato [*digitale.*](../secgloss/d-gly.md)

**L'oggetto Certificates** espone le interfacce seguenti:

-   **ICertificates2:** introdotto in CAPICOM 2.0.
-   **ICertificates:** introdotto in CAPICOM 1.0.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto** Certificates viene usato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un [**oggetto Certificate**](certificate.md) da o verso la raccolta.
-   Generare un subset della raccolta trovando un set di certificati o visualizzando una finestra di dialogo per selezionare i certificati.
-   Cancellare tutti gli [**oggetti Certificate**](certificate.md) dalla raccolta.
-   Recuperare il numero di certificati nella raccolta.
-   Recuperare un [**oggetto Certificate**](certificate.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto Certificates** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Certificates** dispone di questi metodi.



| Metodo                                | Descrizione                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](certificates-add.md)       | Aggiunge un [**oggetto Certificate**](certificate.md) alla raccolta.<br/> (Ereditato da **CertificatesICertificates2**)                                        |
| [**Cancella**](certificates-clear.md)   | Rimuove tutti [**gli oggetti Certificate**](certificate.md) dalla raccolta.<br/> (Ereditato da **CertificatesICertificates2**)                                |
| [**Find**](certificates-find.md)     | Restituisce un **oggetto Certificates** che contiene tutti i certificati che corrispondono ai criteri di ricerca specificati.<br/> (Ereditato da **CertificatesICertificates2**) |
| [**Rimuovi**](certificates-remove.md) | Rimuove un singolo [**oggetto Certificate**](certificate.md) dalla raccolta.<br/> (Ereditato da **CertificatesICertificates2**)                            |
| [**Salva**](certificates-save.md)     | Salva i certificati in un file specificato.<br/> (Ereditato da **CertificatesICertificates2**)                                                                |
| [**Seleziona**](certificates-select.md) | Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati.<br/> (Ereditato da **CertificatesICertificates2**)  |



 

### <a name="properties"></a>Proprietà

**L'oggetto Certificates** ha queste proprietà.



| Proprietà                                             | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](certificates-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di [**oggetti Certificate**](certificate.md) nella raccolta.<br/>                                                                                                                                |
| [**Elemento**](certificates-item.md)<br/>         | Sola lettura<br/> | Recupera un [**oggetto Certificate**](certificate.md) che rappresenta il certificato indicizzato della raccolta. Si tratta della proprietà predefinita.<br/> Ereditato da **CertificatesICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Commenti

**L'oggetto Certificates** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto Certificates** è "CAPICOM. Certificates.2".

**CAPICOM 1. *x*:** ProgID per l'oggetto **Certificates** è "CAPICOM. Certificates.1".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
