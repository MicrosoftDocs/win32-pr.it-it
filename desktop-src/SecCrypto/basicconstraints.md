---
description: Rappresenta l'estensione dei vincoli di base di un certificato.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Oggetto BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8cda73c4a698d40a602b39fd7822dabfbded9a7a35c27db16ca74f7993f7f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879521"
---
# <a name="basicconstraints-object"></a>Oggetto BasicConstraints

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

**L'oggetto BasicConstraints** rappresenta l'estensione dei vincoli di base di un certificato.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto BasicConstraints** viene usato per eseguire le attività seguenti:

-   Determinare se l'estensione dei vincoli di base è presente.
-   Determinare se l'estensione dei vincoli di base è contrassegnata come critica.
-   Determinare se il certificato è vincolato alle autorità di certificazione.
-   Determinare se il vincolo di lunghezza del percorso è presente e recuperare il valore del vincolo di lunghezza del percorso.

## <a name="members"></a>Membri

**L'oggetto BasicConstraints** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto BasicConstraints** ha queste proprietà.



| Proprietà                                                                                     | Tipo di accesso          | Descrizione                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCertificateAuthority**](basicconstraints-iscertificateauthority.md)<br/>         | Sola lettura<br/> | Recupera un valore booleano che indica se il certificato è per [*un'autorità di certificazione*](../secgloss/c-gly.md) (CA).<br/> |
| [**IsCritical**](basicconstraints-iscritical.md)<br/>                                 | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione del vincolo di base è contrassegnata come critica.<br/>                                                                                                     |
| [**IsPathLenConstraintPresent**](basicconstraints-ispathlenconstraintpresent.md)<br/> | Sola lettura<br/> | Recupera un valore booleano che indica se il vincolo di lunghezza del percorso del certificato è presente.<br/>                                                                                                   |
| [**IsPresent**](basicconstraints-ispresent.md)<br/>                                   | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione dei vincoli di base è presente. Si tratta della proprietà predefinita.<br/>                                                                              |
| [**PathLenConstraint**](basicconstraints-pathlenconstraint.md)<br/>                   | Sola lettura<br/> | Recupera il valore del vincolo di lunghezza del percorso.<br/>                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto BasicConstraints.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti di crittografia](cryptography-objects.md)
</dt> </dl>

 

 
