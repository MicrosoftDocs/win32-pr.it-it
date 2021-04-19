---
description: Un servizio non deve accedere all' \_ utente corrente di HKEY \_ o alla radice delle \_ classi HKEY \_ , soprattutto quando si rappresenta un utente. Usare invece la funzione RegOpenCurrentUser o RegOpenUserClassesRoot.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Servizi e registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317670"
---
# <a name="services-and-the-registry"></a>Servizi e registro di sistema

Un servizio non deve accedere **all' \_ \_ utente corrente di HKEY** o alla **\_ \_ radice delle classi HKEY**, soprattutto quando si rappresenta un utente. Usare invece la funzione [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) o [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .

Se si tenta di accedere **all' \_ \_ utente corrente di HKEY** o alla **\_ \_ radice delle classi HKEY** da un servizio, potrebbe non riuscire o potrebbe sembrare funzionante, ma esiste una perdita sottostante che può causare problemi durante il caricamento o lo scaricamento del profilo utente.

 

 
