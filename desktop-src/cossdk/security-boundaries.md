---
description: La sicurezza viene verificata solo ai limiti dell'applicazione.
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: Limiti di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050be064c8a2fe3dc8eb81e2297e1699504f92ae7b8b4352d9b875dfc50e91a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047269"
---
# <a name="security-boundaries"></a>Limiti di sicurezza

La sicurezza viene verificata solo ai limiti dell'applicazione. In altre parole, per due componenti nella stessa applicazione, quando un componente chiama l'altro, non verrà eseguito alcun controllo di sicurezza. Tuttavia, se due applicazioni condividono lo stesso processo e un componente in una chiama un componente nell'altra, viene eseguito un controllo di sicurezza perché viene oltrepassato un limite dell'applicazione. Analogamente, se due applicazioni risiedono in processi server diversi e un componente nella prima applicazione chiama un componente nella seconda applicazione, viene eseguito un controllo di sicurezza.

Pertanto, se si dispone di due componenti e si vuole che i controlli di sicurezza siano eseguiti quando uno chiama l'altro, è necessario inserire i componenti in applicazioni COM+ separate.

Poiché le applicazioni di libreria COM+ sono ospitate da altri processi, esiste un limite di sicurezza tra l'applicazione libreria e il processo di hosting. Inoltre, l'applicazione libreria non controlla la sicurezza a livello di processo, che influisce su come è necessario configurarla. Per altre informazioni, vedere [Sicurezza delle applicazioni della libreria.](library-application-security.md)

Determinare se un controllo di sicurezza deve essere eseguito in una chiamata a un componente si basa sulla proprietà di sicurezza nel contesto dell'oggetto creato quando viene creata un'istanza del componente configurato. Per altre informazioni, vedere [Proprietà del contesto di sicurezza](security-context-property.md).

## <a name="component-level-access-checks"></a>Component-Level di accesso

Per un'applicazione server COM+, è possibile scegliere di forzare i controlli di accesso a livello di componente o di processo.

Quando si seleziona il controllo dell'accesso a livello di componente, si abilitano le assegnazioni di ruolo con granularità fine. È possibile assegnare ruoli a componenti, interfacce e metodi e ottenere criteri di autorizzazione articolati. Questa sarà la configurazione standard per le applicazioni che usano la sicurezza basata sui ruoli.

Per le applicazioni libreria COM+, è necessario selezionare sicurezza a livello di componente se si vogliono usare i ruoli. Le applicazioni di libreria non possono usare la sicurezza a livello di processo.

È consigliabile selezionare controllo di accesso a livello di componente se si usa la sicurezza basata su ruoli a livello di codice. Le informazioni sul contesto di chiamata di sicurezza sono disponibili solo quando è abilitata la sicurezza a livello di componente. Per altre informazioni, vedere [Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).

Inoltre, quando si seleziona il controllo di accesso a livello di componente, la proprietà di sicurezza verrà inclusa nel contesto dell'oggetto. Ciò significa che la configurazione della sicurezza può svolgere un ruolo nella modalità di attivazione dell'oggetto. Per altre informazioni, vedere [Proprietà del contesto di sicurezza](security-context-property.md).

## <a name="process-level-access-checks"></a>Process-Level di accesso

I controlli a livello di processo si applicano solo al limite dell'applicazione. In altre informazioni, i ruoli definiti per l'intera applicazione COM+ determineranno a chi viene concesso l'accesso a qualsiasi risorsa all'interno dell'applicazione. Non vengono applicate assegnazioni di ruolo con granularità più fine. Essenzialmente, i ruoli vengono usati per creare un descrittore di sicurezza rispetto al quale viene convalidata qualsiasi chiamata ai componenti dell'applicazione. In questo caso, non è necessario creare criteri di autorizzazione dettagliati con più ruoli. L'applicazione userà un singolo descrittore di sicurezza.

Per le applicazioni libreria COM+, non è necessario selezionare i controlli di accesso a livello di processo. L'applicazione libreria verrà eseguita ospitata nel processo del client e pertanto non controlla la sicurezza a livello di processo. Per altre informazioni, vedere [Sicurezza delle applicazioni della libreria.](library-application-security.md)

Con i controlli di accesso a livello di processo abilitati, le informazioni sul contesto delle chiamate di sicurezza non sono disponibili. Ciò significa che non è possibile eseguire la sicurezza a livello di codice quando si usa solo la sicurezza a livello di processo. Per altre informazioni, vedere [Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).

Inoltre, la proprietà di sicurezza non verrà inclusa nel contesto dell'oggetto. Ciò significa che quando si usano solo controlli di accesso a livello di processo, la configurazione della sicurezza non avrà mai un ruolo nella modalità di attivazione dell'oggetto. Per altre informazioni, vedere [Proprietà del contesto di sicurezza](security-context-property.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione efficace dei ruoli](designing-roles-effectively.md)
</dt> <dt>

[Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md)
</dt> <dt>

[Proprietà del contesto di sicurezza](security-context-property.md)
</dt> <dt>

[Uso dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



