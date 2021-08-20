---
description: Descrive le impostazioni dei criteri di risparmio energia che costituiscono una combinazione per il risparmio di energia.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Criteri di Impostazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f8c0dbd4c7f2a27b6e6b96528c689c6609c175eded58a1de625af71e965f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674311"
---
# <a name="power-policy-settings"></a>Criteri di Impostazioni

Combinazioni per il risparmio di energia e schemi sono costituiti da preferenze e impostazioni dei criteri.

Una combinazione per il risparmio di energia è costituita da un gruppo di preferenze per le impostazioni di risparmio energia. Queste preferenze sono costituite sia da un valore AC che da un valore DC per ognuna delle impostazioni di risparmio energia. Ogni combinazione per il risparmio di energia viene identificata **tramite un GUID** univoco e un nome descrittivo. Windows Vista ha tre combinazioni per il risparmio di energia predefinite: Risparmio di energia, Bilanciato e Prestazioni elevate. Questi piani possono essere personalizzati ed è possibile creare piani aggiuntivi. Tutte le combinazioni per il risparmio di energia hanno un attributo di personalità che indica il comportamento complessivo di risparmio energetico del piano.

La tabella seguente illustra le tre personalità della combinazione per il risparmio di energia. 

| Nome visualizzato     | Descrizione                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Risparmio energia      | Offre prestazioni ridotte che possono aumentare il risparmio di energia.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Balanced         | Bilancia automaticamente le prestazioni e il consumo energetico in base alla domanda. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Prestazioni elevate | Offre prestazioni massime a scapito di un maggiore consumo di energia.      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> I dispositivi che [supportano la modalità Standby](/windows-hardware/design/device-experiences/modern-standby) moderno consentono solo la **combinazione per il risparmio di** energia Bilanciata. **Modern Standby è** la soluzione più recente e semplificata per la gestione delle impostazioni di risparmio energia.

 

Ogni computer ha una singola combinazione per il risparmio di energia attiva. Per impostazione predefinita, gli utenti senza privilegi sono in grado di accedere alle impostazioni di risparmio energia del sistema. L'accesso a tutte le impostazioni di risparmio energia o a singole impostazioni di risparmio energia può essere controllato tramite ACL nelle impostazioni di risparmio energia o tramite Criteri di gruppo. Le applicazioni devono chiamare [**PowerSettingAccessCheck per**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) determinare se l'utente ha accesso all'impostazione di risparmio energia.

Ogni impostazione di risparmio energia è identificata da un **GUID univoco** e include un nome descrittivo, una descrizione, i valori consentiti e i valori predefiniti per AC e DC. È possibile creare impostazioni di risparmio energia personalizzate usando [**la funzione PowerCreateSetting.**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazioni per il risparmio di energia](power-schemes.md)
</dt> </dl>

 

 
