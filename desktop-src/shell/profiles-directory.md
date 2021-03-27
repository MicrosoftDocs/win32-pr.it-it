---
description: 'Il sistema archivia le informazioni sul profilo utente in una directory specifica, che ha nomi diversi in versioni diverse di Windows: &\# 0034; Documents and Settings&\# 0034; in Windows XP e &\# 0034; Utenti&\# 0034; in Windows Vista e versioni successive.'
title: Directory profili
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979951"
---
# <a name="profiles-directory"></a>Directory profili

Il sistema archivia le informazioni sul profilo utente in una directory specifica, che ha nomi diversi in versioni diverse di Windows: "Documents and Settings" in Windows XP e "Users" in Windows Vista e versioni successive. Per ottenere il percorso della directory dei profili, usare la funzione [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .

La directory dei profili contiene le sottodirectory seguenti per i profili utente.



| Directory                                      | Descrizione                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ProgramData (Windows Vista o versione successiva) utenti | Informazioni sul programma applicabili a tutti gli utenti. La directory tutti gli utenti è ancora presente in Windows Vista o versione successiva per compatibilità con le versioni precedenti. |
| Predefinito                                        | Informazioni sul profilo valide per l'utente predefinito.                                                                                      |
| *Utente*                                         | Informazioni sul profilo valide per l'utente specificato. Ogni utente dispone di una propria sottodirectory di profilo.                                      |



 

Per ottenere il percorso della directory ProgramData/All Users, chiamare la funzione [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) . La directory contiene le sottodirectory seguenti:



| Directory  | Descrizione                          |
|------------|--------------------------------------|
| Desktop    | Collegamenti da visualizzare sul desktop. |
| Menu Start | Voci di menu per il menu **Start** .   |



 

Per ottenere il percorso della directory dell'utente predefinito, chiamare la funzione [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) . Per ottenere il percorso della directory di un utente specifico, chiamare la funzione [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) . Sia l'utente predefinito che le directory utente specifiche contengono le sottodirectory seguenti. Le directory in corsivo indicano directory nascoste per impostazione predefinita. È possibile visualizzare queste directory selezionando l'opzione **Mostra i file nascosti, le cartelle e le unità** nell'elemento del pannello di controllo **Opzioni cartella** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Directory</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dati applicazione</td>
<td>Dati specifici dell'applicazione.</td>
</tr>
<tr class="even">
<td>Cookie</td>
<td>Cookie di Windows Internet Explorer.</td>
</tr>
<tr class="odd">
<td>Desktop</td>
<td>Collegamenti da visualizzare sul desktop.</td>
</tr>
<tr class="even">
<td>Preferiti</td>
<td>Collegamenti ai siti Web preferiti.</td>
</tr>
<tr class="odd">
<td>Impostazioni locali</td>
<td>Impostazioni e dati dell'applicazione che non eseguono il roaming con il profilo. In genere le impostazioni o i dati in questa directory sono specifici del computer o sono troppo grandi per il roaming efficace. Questa directory contiene le sottocartelle seguenti:
<ul>
<li>Dati applicazione</li>
<li>Cronologia</li>
<li>Temp</li>
<li>File temporanei di Internet</li>
</ul></td>
</tr>
<tr class="even">
<td>Documenti</td>
<td>Il percorso predefinito per i documenti creati dall'utente. Per impostazione predefinita, le applicazioni devono salvare i file di documento in questa directory.</td>
</tr>
<tr class="odd">
<td><em>NetHood</em></td>
<td>Collegamenti agli elementi del quartiere di rete.</td>
</tr>
<tr class="even">
<td><em>PrintHood</em></td>
<td>Collegamenti agli elementi della cartella della stampante.</td>
</tr>
<tr class="odd">
<td><em>Origini</em></td>
<td>Collegamenti ai documenti utilizzati più di recente.</td>
</tr>
<tr class="even">
<td>SendTo</td>
<td>Collegamenti ai percorsi a cui l'utente invia spesso i file.</td>
</tr>
<tr class="odd">
<td>Menu Start</td>
<td>Voci di menu per il menu <strong>Start</strong> .</td>
</tr>
<tr class="even">
<td><em>Modelli</em></td>
<td>Collegamenti agli elementi del modello.</td>
</tr>
</tbody>
</table>



 

Per ottenere il percorso delle sottodirectory di queste directory, usare le funzioni [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) o [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

 

 



