---
description: 'Questa sezione relativa ai tipi di file e alle associazioni di file è organizzata nel modo seguente:'
ms.assetid: 45d8b729-1e9d-40c0-8306-9a475262ac40
title: Tipi di file e associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf84bbf44475d32768d2359d3723952ada843c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227453"
---
# <a name="file-types-and-file-associations"></a>Tipi di file e associazioni di file

Questa sezione relativa ai tipi di file e alle associazioni di file è organizzata nel modo seguente:

-   [Registrazione dell'applicazione](app-registration.md)
-   [Tipi di file](fa-file-types.md)
-   [Come scegliere un'estensione del tipo di file](how-to-choose-a-file-type-extension.md)
-   [Come definire gli attributi del tipo di file](how-to-define-file-type-attributes.md)
-   [Come includere un'applicazione nella finestra di dialogo Apri con](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)
-   [Funzionamento delle associazioni di file](fa-how-work.md)
-   [Visualizzazione contenuto per tipo di file o tipo](prophand-content-view.md)
-   [Come registrare le proprietà personalizzate e il layout per il tipo di file](how-to-register-custom-properties-and-layout-for-your-file-type.md)
-   [Tipo di file Verifier](file-type-verifier.md)
-   [Come utilizzare il tipo di file Verifier](how-to-use-the-file-type-verifier.md)
-   [Gestori di tipi di file](fa-file-extensions.md)
-   [Identificatori a livello di codice](fa-progids.md)
-   [Come registrare un tipo di file per una nuova applicazione](how-to-register-a-file-type-for-a-new-application.md)
-   [Tipi percepiti](fa-perceivedtypes.md)
-   [Matrici di associazione](fa-associationarray.md)

## <a name="additional-resources"></a>Risorse aggiuntive

-   Set Program Access e computer Defaults (SPAD) è un pannello di controllo di Windows che consente agli utenti con privilegi amministrativi di impostare un'impostazione predefinita del computer e nascondere o visualizzare un'applicazione. Le applicazioni multimediali, di posta elettronica, browser, Messenger e Java sono esempi di applicazioni registrate in SPAD. Impostare i programmi predefiniti (Imposta programmi predefiniti) è un pannello di controllo di Windows, che funziona con privilegi limitati e consente agli utenti di impostare un valore predefinito per l'utente. Qualsiasi applicazione può eseguire la registrazione in Imposta programmi predefiniti. Per informazioni sulla registrazione dell'applicazione SPAD e imposta programmi predefiniti, vedere [linee guida per le associazioni di file e programmi predefiniti](appguide-fa-defpro.md)e [impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md).
-   Per informazioni di base concettuali correlate, vedere [Cenni preliminari sui verbi e sulle associazioni di file](fa-verbs.md).
-   Per creare un archivio dati della shell, vedere [Implementing the Basic Folder Object Interfaces](nse-implement.md).

Per la documentazione di riferimento correlata, vedere gli argomenti seguenti:

-   Per eseguire un verbo su un elemento della shell, vedere il metodo [**InvokeVerb**](folderitem-invokeverb.md) .
-   Per recuperare una raccolta di verbi che possono essere eseguiti su un elemento della shell, vedere il metodo [**verbs**](folderitem-verbs.md) .
-   Per eseguire un'operazione su un file specificato, vedere le funzioni [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .
-   Per un elenco di tipi percepiti predefiniti, vedere l'enumerazione [**percepita**](/windows/win32/api/shtypes/ne-shtypes-perceived) .
-   Per recuperare il tipo percepito di un file in base alla relativa estensione, vedere la funzione [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .

 

 



