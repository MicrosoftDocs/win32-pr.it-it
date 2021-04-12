---
description: Windows Installer offre agli sviluppatori di pacchetti la possibilità di creare un'interfaccia utente interna con più livelli di funzionalità.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Livelli di interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234020"
---
# <a name="user-interface-levels"></a>Livelli di interfaccia utente

Windows Installer offre agli sviluppatori di pacchetti la possibilità di creare un'interfaccia utente interna con più livelli di funzionalità. Poiché l'interfaccia utente interna deve essere creata dall'autore del pacchetto, il comportamento dell'interfaccia utente completa, l'interfaccia utente ridotta, l'interfaccia utente di base e i livelli nessuno dipendono dal pacchetto di installazione. Nella tabella seguente vengono descritte le funzionalità comunemente attribuite ai livelli dell'interfaccia utente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Livello interfaccia utente</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Interfaccia utente completa</td>
<td>Consente di visualizzare le finestre di dialogo modali e non modali che sono state create nell'interfaccia utente interna. Visualizza le finestre di <a href="error-dialog.md">dialogo di errore</a> creati.
<blockquote>
[!Note]<br />
Le finestre di dialogo modali richiedono l'input dell'utente prima di poter continuare l'installazione e vengono specificate impostando il <a href="modal-dialog-style-bit.md">bit di stile della finestra</a> di dialogo modale nella colonna attributi della tabella della finestra di <a href="dialog-table.md">dialogo</a> . Una finestra di dialogo non modale non richiede l'input dell'utente per continuare l'installazione.
</blockquote>
<br/> Un'interfaccia utente completa comunemente presenta il <a href="user-interface-wizard-behavior.md">comportamento della procedura guidata dell'interfaccia utente</a>.<br/></td>
</tr>
<tr class="even">
<td>Interfaccia utente ridotta</td>
<td>Visualizza tutte le finestre di dialogo non modali che sono state create nell'interfaccia utente. Non vengono visualizzate finestre di dialogo modali create. Visualizza le finestre di <a href="error-dialog.md">dialogo di errore</a> creati. Visualizza i messaggi di <a href="authoring-disk-prompt-messages.md">richiesta del disco</a> . Visualizza le finestre di <a href="filesinuse-dialog.md">dialogo Filesinusale</a> .</td>
</tr>
<tr class="odd">
<td>Interfaccia utente di base</td>
<td>Consente di visualizzare le finestre di dialogo non modali incorporate che mostrano i messaggi di stato. Consente di visualizzare le finestre di dialogo di errore predefinite. Non vengono visualizzate finestre di dialogo Create. Richiede agli utenti di inserire un disco visualizzando una finestra di dialogo contenente il valore della proprietà <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</td>
</tr>
<tr class="even">
<td>nessuno</td>
<td>None indica un'installazione invisibile all'utente che non visualizza alcuna interfaccia utente.</td>
</tr>
</tbody>
</table>



 

Il livello dell'interfaccia utente interna può essere impostato tramite [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). Il programma di installazione imposta la proprietà [**UILevel**](uilevel.md) sul livello corrente dell'interfaccia utente.

Se la proprietà [**LIMITUI**](limitui.md) è impostata, il livello di interfaccia utente utilizzato durante l'installazione del pacchetto è limitato a Basic.

Per un esempio di creazione dell'interfaccia utente, vedere [un esempio di installazione](an-installation-example.md).

 

 




