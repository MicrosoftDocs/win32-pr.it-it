---
description: La sicurezza viene controllata solo ai limiti dell'applicazione.
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: Limiti di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcfca8868677ba14c8544657aa77acf04262805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305209"
---
# <a name="security-boundaries"></a>Limiti di sicurezza

La sicurezza viene controllata solo ai limiti dell'applicazione. Ovvero, per due componenti nella stessa applicazione, quando un componente chiama l'altro, non viene eseguito alcun controllo di sicurezza. Tuttavia, se due applicazioni condividono lo stesso processo e un componente in uno chiama un componente nell'altro, viene eseguito un controllo di sicurezza perché viene superato il limite dell'applicazione. Analogamente, se due applicazioni si trovano in processi server diversi e un componente nella prima applicazione chiama un componente nella seconda applicazione, viene eseguito un controllo di sicurezza.

Pertanto, se si dispone di due componenti e si desidera che i controlli di sicurezza vengano eseguiti quando uno chiama l'altro, è necessario inserire i componenti in applicazioni COM+ separate.

Poiché le applicazioni di libreria COM+ sono ospitate da altri processi, esiste un limite di sicurezza tra l'applicazione libreria e il processo di hosting. Inoltre, l'applicazione libreria non controlla la sicurezza a livello di processo, che influiscono sul modo in cui è necessario configurare la sicurezza. Per ulteriori informazioni, vedere la pagina relativa alla [sicurezza delle applicazioni di libreria](library-application-security.md).

Determinare se è necessario eseguire un controllo di sicurezza in una chiamata a un componente è basato sulla proprietà di sicurezza nel contesto dell'oggetto creato quando viene creata un'istanza del componente configurato. Per altre informazioni, vedere [proprietà del contesto di sicurezza](security-context-property.md).

## <a name="component-level-access-checks"></a>Controlli di accesso Component-Level

Per un'applicazione server COM+, è possibile scegliere di applicare i controlli di accesso a livello di componente o a livello di processo.

Quando si seleziona il controllo dell'accesso a livello di componente, si abilitano le assegnazioni di ruolo con granularità fine. È possibile assegnare ruoli a componenti, interfacce e metodi e ottenere un criterio di autorizzazione articolato. Questa sarà la configurazione standard per le applicazioni che usano la sicurezza basata sui ruoli.

Per le applicazioni di libreria COM+, è necessario selezionare sicurezza a livello di componente se si desidera utilizzare i ruoli. Le applicazioni di libreria non possono utilizzare la sicurezza a livello di processo.

Se si usa la sicurezza basata sui ruoli a livello di codice, è necessario selezionare il controllo di accesso a livello di componente. Le informazioni sul contesto delle chiamate di sicurezza sono disponibili solo quando è abilitata la sicurezza a livello di componente. Per ulteriori informazioni, vedere [informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).

Inoltre, quando si seleziona il controllo dell'accesso a livello di componente, la proprietà di sicurezza sarà inclusa nel contesto dell'oggetto. Ciò significa che la configurazione della sicurezza può svolgere un ruolo nella modalità di attivazione dell'oggetto. Per altre informazioni, vedere [proprietà del contesto di sicurezza](security-context-property.md).

## <a name="process-level-access-checks"></a>Controlli di accesso Process-Level

I controlli a livello di processo si applicano solo al limite dell'applicazione. Ovvero i ruoli definiti per l'intera applicazione COM+ determineranno a chi viene concesso l'accesso a tutte le risorse all'interno dell'applicazione. Non vengono applicate assegnazioni di ruolo con granularità fine. I ruoli vengono essenzialmente usati per creare un descrittore di sicurezza in base al quale viene convalidata qualsiasi chiamata ai componenti dell'applicazione. In questo caso, non si desidera creare criteri di autorizzazione dettagliati con più ruoli. L'applicazione utilizzerà un singolo descrittore di sicurezza.

Per le applicazioni della libreria COM+, non è possibile selezionare i controlli di accesso a livello di processo. L'applicazione di libreria viene eseguita nel processo del client e pertanto non controlla la sicurezza a livello di processo. Per ulteriori informazioni, vedere la pagina relativa alla [sicurezza delle applicazioni di libreria](library-application-security.md).

Con i controlli di accesso a livello di processo abilitati, le informazioni sul contesto delle chiamate di sicurezza non sono disponibili. Ciò significa che non è possibile eseguire la sicurezza a livello di codice quando si usa solo la sicurezza a livello di processo. Per ulteriori informazioni, vedere [informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md).

Inoltre, la proprietà di sicurezza non verrà inclusa nel contesto dell'oggetto. Ciò significa che quando si usano solo i controlli di accesso a livello di processo, la configurazione della sicurezza non ridurrà mai un ruolo nella modalità di attivazione dell'oggetto. Per altre informazioni, vedere [proprietà del contesto di sicurezza](security-context-property.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione efficace dei ruoli](designing-roles-effectively.md)
</dt> <dt>

[Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md)
</dt> <dt>

[Proprietà del contesto di sicurezza](security-context-property.md)
</dt> <dt>

[Utilizzo dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



