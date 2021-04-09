---
title: Read-Only i controller di dominio e lo schema di Active Directory
description: Windows Server 2008 introduce un nuovo tipo di controller di dominio, il controller di dominio di sola lettura (RODC).
ms.assetid: 9d9082d2-6f7f-4ffa-b8c7-6414be764d0c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4284ffdda7ed2fbe481c201f7da69371209ce55
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104118606"
---
# <a name="read-only-dcs-and-the-active-directory-schema"></a>Read-Only i controller di dominio e lo schema di Active Directory

Windows Server 2008 introduce un nuovo tipo di controller di dominio, il controller di dominio di sola lettura (RODC). In questo modo viene fornito un controller di dominio da utilizzare nelle succursali in cui non è possibile inserire un controller di dominio completo. Lo scopo è quello di consentire agli utenti delle succursali di accedere ed eseguire attività come la condivisione di file/stampanti anche in assenza di connettività di rete per i siti hub.

Il RODC non modifica la modalità di utilizzo dello schema. È tuttavia utile ricordare che lo schema supporta un Read-Only set di attributi parziali (RO-PAS), noto anche come set di attributi filtrati di RODC, che è un set di attributi speciale che non viene replicato in RODC per motivi di sicurezza. RO-PAS viene definito nello schema tramite l'attributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .

## <a name="rodc-filtered-attribute-set"></a>Set di attributi filtrati RODC

Alcune applicazioni che usano [Active Directory Domain Services](active-directory-domain-services.md) come archivio dati possono avere dati di tipo credenziali, ad esempio password, credenziali o chiavi di crittografia, che non devono essere archiviati in un controller di dominio Read-Only se il controller di dominio di sola lettura viene rubato o compromesso. Per questo tipo di applicazione, è possibile aggiungere l'attributo al set di attributi filtrati di RODC per impedire che venga replicato in RODC nella foresta e contrassegnare l'attributo come riservato, che consente di rimuovere la possibilità di leggere i dati per i membri del gruppo Authenticated Users (incluso qualsiasi RODC).

## <a name="adding-attributes-to-the-rodc-filtered-attribute-set"></a>Aggiunta di attributi al set di attributi filtrati di RODC

Il set di attributi filtrati di RODC è un set dinamico di attributi che non viene replicato in alcun RODC nell'insieme di strutture. È possibile configurare l'attributo del controller di dominio di sola lettura impostato su un master schema che esegue Windows Server 2008. Quando si impedisce la replica degli attributi in RODC, i dati non possono essere esposti inutilmente se un RODC viene rubato o compromesso.

Non è possibile aggiungere attributi critici del sistema al set di attributi filtrati di RODC. Un attributo è critico per il sistema se è necessario per servizi di dominio Active Directory, autorità di protezione locale (LSA), gestione account di sicurezza (SAM) e qualsiasi provider di servizi di sicurezza specifici di Microsoft, ad esempio il protocollo di autenticazione Kerberos, per il corretto funzionamento. Nelle versioni di Windows Server 2008 dopo la beta 3, un attributo critico del sistema ha un valore di attributo schemaFlagsEx di (valore dell'attributo schemaFlagsEx & 0x1 = **true**).

Per istruzioni dettagliate sull'aggiunta di attributi al set di attributi filtrati di RODC, vedere [l'Appendice D della Guida dettagliata relativa a RODC]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10)).

## <a name="marking-attributes-as-confidential"></a>Contrassegno degli attributi come riservati

Inoltre, è consigliabile contrassegnare come riservato tutti gli attributi configurati come parte del set di attributi filtrati di RODC. Per contrassegnare un attributo come riservato, è necessario rimuovere l'autorizzazione di lettura per l'attributo per il gruppo Authenticated Users. Contrassegnare l'attributo come riservato fornisce un'ulteriore protezione contro un RODC compromesso rimuovendo le autorizzazioni necessarie per leggere i dati di tipo credenziale. Per ulteriori informazioni su come contrassegnare gli attributi come riservati, vedere [l'articolo 922836 della Microsoft Knowledge base]( https://support.microsoft.com/kb/922836).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida dettagliata per i controller di dominio di sola lettura]( https://support.microsoft.com/kb/922836)
</dt> </dl>

 

 