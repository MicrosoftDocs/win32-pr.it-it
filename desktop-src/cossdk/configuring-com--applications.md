---
description: Un'applicazione COM+ è essenzialmente un costrutto dichiarativo che consente di configurare un numero qualsiasi di componenti in comune. È ad esempio possibile configurare i componenti di un'applicazione con criteri di sicurezza comuni.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configurazione di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304633"
---
# <a name="configuring-com-applications"></a>Configurazione di applicazioni COM+

Un'applicazione COM+ è essenzialmente un costrutto dichiarativo che consente di configurare un numero qualsiasi di componenti in comune. È ad esempio possibile configurare i componenti di un'applicazione con criteri di sicurezza comuni.

La configurazione è una parte essenziale del processo di sviluppo per le applicazioni COM+. La modalità di configurazione di un'applicazione determinerà il modo in cui COM+ fornirà servizi e il suo comportamento durante l'esecuzione.

È possibile configurare le applicazioni COM+ utilizzando lo strumento di amministrazione Servizi componenti o gli oggetti e le interfacce di amministrazione con script che forniscono la funzionalità sottostante dello strumento di amministrazione. Per informazioni dettagliate sull'esecuzione di amministrazione con script, vedere [automazione di com+ Administration](automating-com--administration.md).

È possibile configurare gli elementi ai livelli seguenti all'interno delle applicazioni COM+:

-   [Impostazioni a livello di applicazione](#application-level-settings)
-   [Impostazioni a livello di componente (a livello di classe)](#component-level-class-level-settings)
-   [Impostazione a livello di interfaccia](#interface-level-setting)
-   [Impostazione a livello di metodo](#method-level-setting)
-   [Argomenti correlati](#related-topics)

La modalità di installazione dei componenti in un'applicazione può influire sul modo in cui è possibile configurarle. È necessario installare sempre i componenti in applicazioni COM+, anziché importarli. L'installazione dei componenti li registrerà completamente, insieme alle interfacce e alle librerie dei tipi, nel database di registrazione della classe COM+ (RegDB) in modo che sia possibile configurarli.

## <a name="application-level-settings"></a>Impostazioni Application-Level



| Attributo                                                                                        | Descrizione                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Activation](context-activation.md)<br/>                                                  | Specifica il tipo di applicazione, ovvero applicazione server o applicazione libreria.<br/>                                                                                                            |
| [Abilitazione di controlli di accesso](enabling-access-checks-for-an-application.md)<br/>               | Attiva e disattiva il controllo della sicurezza.<br/>                                                                                                                                                      |
| [Livello di sicurezza](setting-a-security-level-for-access-checks.md)<br/>                      | Specifica che i controlli di accesso verranno eseguiti a livello di processo (livelli di controllo di accesso generati da ruoli) o sia a livello di processo che a livello di componente (sicurezza completa basata sui ruoli).<br/> |
| [Livello di autenticazione](setting-an-authentication-level-for-a-server-application.md)<br/>  | Imposta il livello di autenticazione utilizzato per le chiamate nell'applicazione.<br/>                                                                                                                        |
| [Livello di rappresentazione](setting-an-impersonation-level.md)<br/>                             | Imposta il livello di rappresentazione usato per le chiamate ad altre applicazioni.<br/>                                                                                                                        |
| [Accodamento](creating-queuable-components.md)<br/>                                           | Specifica che i componenti dell'applicazione utilizzeranno i servizi di Accodamento.<br/>                                                                                                                         |
| [Abilita CRM](configuring-com--crm-components.md)<br/>                                     | Consente l'uso di gestione risorse di compensazione.<br/>                                                                                                                                           |
| [Eseguire l'applicazione come servizio](com--applications-running-as-service-applications.md)<br/> | Configura e implementa un'applicazione server COM+ come servizio NT.<br/>                                                                                                                    |
| [Servizio SOAP COM+](com--soap-service.md)<br/>                                            | Espone un'applicazione COM+ come un servizio Web XML.<br/>                                                                                                                                        |
| [Pool di applicazioni](com--application-pooling.md)<br/>                                   | Aggiunge la scalabilità per i processi a thread singolo e si integra con il servizio di riciclo delle applicazioni COM+.<br/>                                                                               |
| [Riciclo delle applicazioni](com--application-recycling.md)<br/>                               | Aumenta la stabilità dell'applicazione arrestando normalmente un processo associato a un'applicazione e riavviarlo.<br/>                                                                  |
| [Dump del processo](what-s-new-in-com--1-5.md)<br/>                                         | Esegue il dump dell'intero stato di un processo senza terminarlo a scopo di debug.<br/>                                                                                                      |
| Arresto del processo server<br/>                                                               | Arresta un processo dopo un periodo di inattività specificato.<br/>                                                                                                                                      |
| Autorizzazioni<br/>                                                                           | Disabilita le modifiche apportate alle impostazioni di configurazione, inclusa l'eliminazione.<br/>                                                                                                                          |
| Identità di sicurezza<br/>                                                                     | Specifica l'identità con cui viene eseguita l'applicazione.<br/>                                                                                                                                 |
| Avvia nel debugger<br/>                                                                    | Specifica che l'applicazione verrà avviata in un debugger, con le impostazioni della riga di comando specificate dall'utente.<br/>                                                                                |
| Abilita supporto 3GB<br/>                                                                    | Consente l'uso dello spazio degli indirizzi di memoria del processo esteso.<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Impostazioni di Component-Level (a livello di classe)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="configuring-transactions.md">Transazioni</a><br/></td>
<td>Imposta i requisiti di transazione automatici disabilitati, non supportati, supportati, necessari o nuovi.<br/></td>
</tr>
<tr class="even">
<td><a href="setting-the-synchronization-attribute.md">Sincronizzazione</a><br/></td>
<td>Imposta i requisiti di sincronizzazione disabilitati, non supportati, supportati, necessari o nuovi.<br/></td>
</tr>
<tr class="odd">
<td><a href="enabling-jit-activation-for-a-component.md">Attivazione JIT</a><br/></td>
<td>Abilita l'attivazione JIT.<br/></td>
</tr>
<tr class="even">
<td><a href="configuring-a-component-to-be-pooled.md">Pooling di oggetti</a><br/></td>
<td>Abilita il pool di oggetti. Le dimensioni minime e massime del pool e i valori di timeout dell'oggetto sono configurabili.<br/></td>
</tr>
<tr class="odd">
<td><a href="specifying-an-object-constructor-string-for-a-component.md">Costruzione di oggetti</a><br/></td>
<td>Consente la costruzione di oggetti con parametri con una stringa del costruttore specificata amministrativamente. <br/>
<blockquote>
[!Note]<br />
La stringa del costruttore non deve essere utilizzata per archiviare informazioni sensibili alla sicurezza.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="enabling-access-checks-at-the-component-level.md">Controlli di accesso a livello di componente</a><br/></td>
<td>Attiva o disattiva il controllo di sicurezza basato sui ruoli a livello di componente.<br/></td>
</tr>
<tr class="odd">
<td><a href="assigning-roles-to-components--interfaces--or-methods.md">Assegnazione di ruolo dichiarativa</a><br/></td>
<td>Consente l'assegnazione esplicita dei ruoli al componente.<br/></td>
</tr>
<tr class="even">
<td><a href="persistent-client-side-failures.md">Classe Exception di Accodamento</a><br/></td>
<td>Indica una classe di eccezioni per la gestione degli errori sul lato client.<br/></td>
</tr>
<tr class="odd">
<td><a href="com--instrumentation-concepts.md">Eventi e statistiche di strumentazione</a><br/></td>
<td>Consente di creare report dettagliati sugli eventi di sistema e sulle statistiche degli oggetti.<br/></td>
</tr>
<tr class="even">
<td><a href="context-activation.md">Contesto di attivazione</a><br/></td>
<td>Abilita l'attivazione forzata di un oggetto nel contesto del chiamante o nel contesto predefinito.<br/></td>
</tr>
<tr class="odd">
<td><a href="what-s-new-in-com--1-5.md">Creazione di componenti privati</a><br/></td>
<td>Contrassegna il componente come privato per l'applicazione. Un componente privato può essere visualizzato e attivato solo da altri componenti nella stessa applicazione.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a>Impostazione Interface-Level



| Attributo                                                                                           | Descrizione                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Queued](creating-queuable-components.md)<br/>                                               | Indica un'interfaccia accodabile, definita in IDL.<br/>                                                                       |
| [Assegnazione di ruolo dichiarativa](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Consente l'assegnazione esplicita dei ruoli all'interfaccia, oltre ai ruoli ereditati in modo implicito dal livello del componente.<br/> |



 

## <a name="method-level-setting"></a>Impostazione Method-Level



| Attributo                                                                                           | Descrizione                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Operazione eseguita automaticamente](enabling-auto-done-for-a-method.md)<br/>                                         | Disattiva automaticamente l'oggetto al ritorno del metodo e i voti nella transazione.<br/>                                                       |
| [Assegnazione di ruolo dichiarativa](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Consente l'assegnazione esplicita dei ruoli al metodo, nonché i ruoli ereditati in modo implicito dai livelli di interfaccia e di componente.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Automazione dell'amministrazione COM+](automating-com--administration.md)
</dt> <dt>

[Creazione di applicazioni COM+](creating-com--applications.md)
</dt> <dt>

[Distribuzione di applicazioni COM+](deploying-com--applications.md)
</dt> </dl>

 

 




