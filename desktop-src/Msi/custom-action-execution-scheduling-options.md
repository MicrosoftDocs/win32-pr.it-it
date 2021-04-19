---
description: Poiché un'azione personalizzata può essere pianificata sia nell'interfaccia utente che nelle tabelle di sequenza di esecuzione e può essere eseguita nel servizio o nel processo client, un'azione personalizzata può essere potenzialmente eseguita più volte.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Opzioni di pianificazione dell'esecuzione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313358"
---
# <a name="custom-action-execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione di azioni personalizzate

Poiché un'azione personalizzata può essere pianificata sia nell'interfaccia utente che nelle tabelle di sequenza di esecuzione e può essere eseguita nel servizio o nel processo client, un'azione personalizzata può essere potenzialmente eseguita più volte.

Si noti che il programma di installazione:

-   Esegue le azioni in una tabella di sequenza immediatamente per impostazione predefinita.
-   Non esegue un'azione se il campo dell'espressione condizionale della tabella di sequenza restituisce false.
-   Elabora la tabella di sequenza dell'interfaccia utente nel processo client se il livello di interfaccia dell'utente interno è impostato sulla modalità di interfaccia utente completa (vedere [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) per una descrizione dei livelli dell'interfaccia utente).
-   È un servizio registrato per impostazione predefinita quando si utilizza Windows 2000 e, in questo caso, la tabella Execute Sequence viene elaborata nel servizio del programma di installazione.

È possibile utilizzare i flag di opzione seguenti per controllare la più immediata esecuzione di azioni personalizzate. Per impostare un'opzione, aggiungere il valore di questa tabella al valore nel campo Type della [tabella CustomAction](customaction-table.md). Nessuno dei seguenti flag deve essere utilizzato con [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md).

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span>predefinita
</dt> <dd>

Esadecimale: 0x00000000

Decimale: 0

Eseguire sempre. L'azione può essere eseguita due volte se presente in entrambe le tabelle di sequenza.

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence** 
</dt> <dd>

Esadecimale: 0x00000100

Decimale: 256

Eseguire non più di una volta se presente in entrambe le tabelle di sequenza. Ignora sempre l'azione nella sequenza di esecuzione se è stata eseguita la sequenza dell'interfaccia utente. Nessun effetto nella sequenza dell'interfaccia utente. Non è necessario che l'azione sia presente o eseguita nella sequenza dell'interfaccia utente da ignorare nella sequenza di esecuzione. Non interessato dalla registrazione del servizio di installazione.

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**
</dt> <dd>

Esadecimale: 0x00000200

Decimale: 512

Eseguire una sola volta per processo se in entrambe le tabelle di sequenza. Ignora l'azione nella sequenza di esecuzione se la sequenza dell'interfaccia utente è stata eseguita nello stesso processo, ad esempio entrambi eseguiti nel processo client. Utilizzato per impedire l'esecuzione di due azioni che modificano lo stato della sessione, ad esempio dati di proprietà e database.

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**
</dt> <dd>

Esadecimale: 0x00000300

Decimale: 768

Eseguire solo se in esecuzione sul client dopo l'esecuzione della sequenza dell'interfaccia utente. L'azione viene eseguita solo se la sequenza di esecuzione viene eseguita nel client seguente sequenza dell'interfaccia utente. Può essere usato per fornire la logica/o oppure per disattivare l'elaborazione correlata all'interfaccia utente, se già eseguita per la sessione client.

</dd> </dl>

Si noti che per eseguire un'azione personalizzata durante due modalità di esecuzione diverse, creare due voci nella [tabella CustomAction](customaction-table.md) . Ad esempio, per eseguire un'azione personalizzata che chiama una libreria di collegamento dinamico (DLL) C/C++ ( [tipo di azione personalizzata 1](custom-action-type-1.md)) quando la modalità è MSIRUNMODE \_ scheduled e MSIRUNMODE \_ rollback, inserire due voci nella tabella CustomAction che chiamano la stessa dll ma con tipi numerici diversi. Includere il codice che chiama [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) per determinare quando eseguire l'azione personalizzata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'azione personalizzata](custom-action-reference.md)
</dt> <dt>

[Informazioni sulle azioni personalizzate](about-custom-actions.md)
</dt> <dt>

[Uso di azioni personalizzate](using-custom-actions.md)
</dt> </dl>

 

 



