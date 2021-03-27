---
description: Viene illustrato come verificare che l'applicazione venga visualizzata nel menu Apri con e nella finestra di dialogo per le applicazioni desktop ed è disponibile come app di Windows Store predefinita per i tipi di file specificati.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Come includere un'applicazione nella finestra di dialogo Apri con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881566"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Come includere un'applicazione nella finestra di dialogo Apri con

Viene illustrato come verificare che l'applicazione venga visualizzata nel menu **Apri con** e nella finestra di dialogo per le applicazioni desktop ed è disponibile come app di Windows Store predefinita per i tipi di file specificati.

## <a name="instructions"></a>Istruzioni

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Per ogni tipo di file, aggiungere l'applicazione alla sottochiave del registro di sistema OpenWithProgIds.

Aggiungere il ProgID come nome di valore, con il tipo di valore REG \_ None o reg \_ SZ e una stringa vuota come valore di dati.

Negli esempi di registro di sistema seguenti vengono illustrate le voci che associano InfoPath e per Microsoft Visual Studio con il tipo di file XML.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Commenti

La sottochiave **OpenWithProgids** è preferibile a **OpenWithList** per identificare un'applicazione. Per ulteriori informazioni su queste sottochiavi, vedere [impostazione di sottochiavi facoltative e attributi di estensione del tipo di file](fa-file-types.md).

**OpenWithList** è destinato solo alle app legacy (solo con estensione exe) nei sistemi operativi precedenti a Windows XP.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



