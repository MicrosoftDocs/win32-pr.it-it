---
description: I moduli merge operano solo con componenti e non con funzionalità. Tuttavia, alcune tabelle nei moduli merge, ad esempio la tabella PublishComponent, contengono campi che fanno riferimento alle funzionalità.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Riferimenti alle funzionalità nei moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967410"
---
# <a name="referencing-features-in-merge-modules"></a>Riferimenti alle funzionalità nei moduli merge

I moduli merge operano solo con componenti e non con funzionalità. Tuttavia, alcune tabelle nei moduli merge, ad esempio la [tabella PublishComponent](publishcomponent-table.md), contengono campi che fanno riferimento alle funzionalità.

Un GUID null: {00000000-0000-0000-0000-000000000000} deve essere creato in qualsiasi campo di un database del modulo merge che fa riferimento a una funzionalità. Quando il modulo merge viene unito in un pacchetto di installazione, lo strumento merge sostituisce il GUID null con la funzionalità specificata nel pacchetto di installazione, ad eccezione delle tabelle che richiedono una gestione speciale, ad esempio la [tabella ModuleSignature](modulesignature-table.md) e le tabelle ModuleSequence.

Si noti che se un GUID null viene utilizzato come chiave primaria, non è garantito che il valore sostituito dallo strumento di merge sia univoco. Gli autori dei moduli merge sono responsabili di garantire che nessuna chiave primaria esistente nell'interfaccia dell'utente venga duplicata quando lo strumento di Unione sostituisce i GUID null con le funzionalità.

 

 



