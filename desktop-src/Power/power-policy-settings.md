---
description: Descrive le impostazioni dei criteri di risparmio energia che costituiscono uno schema di risparmio energia.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Impostazioni di criteri di risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756572"
---
# <a name="power-policy-settings"></a>Impostazioni di criteri di risparmio energia

Combinazioni per il risparmio di energia e schemi sono costituite da preferenze e impostazioni dei criteri.

Una combinazione per il risparmio di energia è costituita da un gruppo di impostazioni di risparmio energia. Queste preferenze sono costituite sia da un valore AC che da un controller di dominio per ogni impostazione di risparmio energia. Ogni combinazione per il risparmio di energia viene identificata tramite un **GUID** univoco e un nome descrittivo. Windows Vista prevede tre combinazioni per il risparmio di energia predefinite: risparmio energia, bilanciato e prestazioni elevate. Questi piani possono essere personalizzati e possono essere creati piani aggiuntivi. Tutte le combinazioni per il risparmio di energia hanno un attributo di personalità che indica il comportamento di risparmio energetico complessivo del piano.

La tabella seguente illustra le tre personali del piano di risparmio energia. 

| Nome visualizzato     | Descrizione                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Risparmio energia      | Offre prestazioni ridotte che possono aumentare il risparmio di energia.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Balanced         | Bilancia automaticamente le prestazioni e il consumo di energia in base alla domanda. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Prestazioni elevate | Offre prestazioni massime a scapito di un consumo di energia superiore.      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> I dispositivi che supportano la modalità [standby moderna](/windows-hardware/design/device-experiences/modern-standby) consentono solo la combinazione per il risparmio di energia **bilanciata** . **Modern standby** è la soluzione più recente e semplificata per la gestione delle impostazioni di risparmio energia.

 

Ogni computer dispone di una singola combinazione per il risparmio di energia attiva. Per impostazione predefinita, gli utenti senza privilegi sono in grado di accedere alle impostazioni di risparmio energia del sistema. L'accesso a tutte le impostazioni di risparmio energia o a singole impostazioni può essere controllato tramite ACL nelle impostazioni di risparmio energia o tramite Criteri di gruppo. Le applicazioni devono chiamare [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) per determinare se l'utente può accedere all'impostazione di risparmio energia.

Ogni impostazione di risparmio energia è identificata da un **GUID** univoco e include un nome descrittivo, una descrizione, valori consentiti e valori predefiniti per AC e DC. È possibile creare impostazioni di risparmio energia personalizzate usando la funzione [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazioni per il risparmio di energia](power-schemes.md)
</dt> </dl>

 

 
