---
description: Gli sviluppatori possono impedire l'immissione di informazioni riservate, ad esempio password, nel file di log durante un'installazione Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Prevenzione della scrittura di informazioni riservate nel file di log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049896"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a>Prevenzione della scrittura di informazioni riservate nel file di log

Quando si usa la Windows Installer, è possibile impedire l'immissione nel file di log di informazioni riservate, ad esempio le password, e renderle visibili.

-   Il programma di installazione non scrive mai le informazioni nella colonna password della [tabella ServiceInstall](serviceinstall-table.md) nel log.
-   È possibile impedire al programma di installazione di scrivere la proprietà associata a un [controllo di modifica](edit-control.md) nel log impostando l' [attributo di controllo delle password](password-control-attribute.md). La proprietà associata a un controllo di modifica con l'attributo di controllo password è nascosta anche se i criteri di [debug](debug.md) sono impostati su un valore pari a 7.
-   È possibile impedire al programma di installazione di scrivere una proprietà privata nel log includendo la proprietà nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) .
    > [!Note]  
    > Questo metodo consente di rendere visibili le informazioni riservate in una riga di comando nel log. Quando il criterio di [debug](debug.md) è impostato su un valore pari a 7, il programma di installazione scriverà le informazioni immesse in una riga di comando nel log. In questo modo la proprietà immessa in una riga di comando è visibile anche se la proprietà è inclusa nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) .

     

-   È possibile impedire che le informazioni nella colonna di destinazione della tabella [CustomAction](customaction-table.md) vengano scritte nel log includendo il flag di bit HideTarget nel campo Type della tabella CustomAction. Il valore di questo flag è 8192 (0x2000). Per altre informazioni, vedere [opzione di destinazione nascosta dell'azione personalizzata](custom-action-hidden-target-option.md).

 

 



