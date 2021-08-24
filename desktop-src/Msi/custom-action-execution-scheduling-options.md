---
description: Poiché un'azione personalizzata può essere pianificata sia nell'interfaccia utente che nelle tabelle di sequenza di esecuzione e può essere eseguita nel servizio o nel processo client, un'azione personalizzata può essere eseguita potenzialmente più volte.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Opzioni di pianificazione dell'esecuzione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91adbee99684a5a9db0701c2371c8c517547b4d91881518d72fe7c25c0d189be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520101"
---
# <a name="custom-action-execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione di azioni personalizzate

Poiché un'azione personalizzata può essere pianificata sia nell'interfaccia utente che nelle tabelle di sequenza di esecuzione e può essere eseguita nel servizio o nel processo client, un'azione personalizzata può essere eseguita potenzialmente più volte.

Si noti che il programma di installazione:

-   Esegue azioni in una tabella di sequenza immediatamente per impostazione predefinita.
-   Non esegue un'azione se il campo dell'espressione condizionale della tabella di sequenza restituisce False.
-   Elabora la tabella della sequenza dell'interfaccia utente nel processo client se il livello di interfaccia utente interno è impostato sulla modalità interfaccia utente completa (vedere [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) per una descrizione dei livelli dell'interfaccia utente).
-   È un servizio registrato per impostazione predefinita quando si usa Windows 2000 e, in questo caso, la tabella della sequenza di esecuzione viene elaborata nel servizio di installazione.

È possibile usare i flag di opzione seguenti per controllare l'esecuzione immediata di azioni personalizzate. Per impostare un'opzione, aggiungere il valore in questa tabella al valore nel campo Tipo della [tabella CustomAction](customaction-table.md). Nessuno dei flag seguenti deve essere usato con le azioni personalizzate [di esecuzione posticipata.](deferred-execution-custom-actions.md)

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span>(impostazione predefinita)
</dt> <dd>

Esadecimale: 0x00000000

Decimale: 0

Eseguire sempre. L'azione può essere eseguita due volte se presente in entrambe le tabelle di sequenza.

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence** 
</dt> <dd>

Esadecimale: 0x00000100

Decimale: 256

Eseguire non più di una volta se presente in entrambe le tabelle di sequenza. Ignora sempre l'azione nella sequenza di esecuzione se è stata eseguita la sequenza dell'interfaccia utente. Nessun effetto nella sequenza dell'interfaccia utente. Non è necessario che l'azione sia presente o eseguita nella sequenza dell'interfaccia utente per essere ignorata nella sequenza di esecuzione. Non interessato dalla registrazione del servizio di installazione.

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**
</dt> <dd>

Esadecimale: 0x00000200

Decimale: 512

Eseguire una sola volta per ogni processo se in entrambe le tabelle di sequenza. Ignora l'azione nella sequenza di esecuzione se la sequenza dell'interfaccia utente è stata eseguita nello stesso processo, ad esempio entrambe eseguite nel processo client. Usato per impedire l'esecuzione di due volte delle azioni che modificano lo stato della sessione, ad esempio i dati di proprietà e di database.

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**
</dt> <dd>

Esadecimale: 0x00000300

Decimale: 768

Eseguire solo se in esecuzione sul client dopo l'esecuzione della sequenza dell'interfaccia utente. L'azione viene eseguita solo se la sequenza di esecuzione viene eseguita nel client che segue la sequenza dell'interfaccia utente. Può essere usato per fornire logica o o per eliminare l'elaborazione correlata all'interfaccia utente, se già eseguita per la sessione client.

</dd> </dl>

Si noti che per eseguire un'azione personalizzata durante due diverse modalità di esecuzione, creare due voci nella [tabella CustomAction](customaction-table.md) . Ad esempio, per avere un'azione personalizzata che chiama una libreria a collegamento dinamico (DLL) C/C++ (Tipo di azione personalizzata [1)](custom-action-type-1.md)sia quando la modalità è MSIRUNMODE SCHEDULED che MSIRUNMODE ROLLBACK, inserire due voci nella tabella CustomAction che chiamano la stessa DLL ma che hanno tipi \_ \_ numerici diversi. Includere il codice che chiama [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) per determinare quando eseguire l'azione personalizzata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su azioni personalizzate](custom-action-reference.md)
</dt> <dt>

[Informazioni sulle azioni personalizzate](about-custom-actions.md)
</dt> <dt>

[Uso di azioni personalizzate](using-custom-actions.md)
</dt> </dl>

 

 



