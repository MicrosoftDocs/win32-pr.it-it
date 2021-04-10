---
description: Se il criterio di sistema per computer è impostato su &\# 0034; 1&\# 0034;, il programma di installazione scrive i messaggi di debug comuni nel debugger usando la funzione OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883006"
---
# <a name="debug"></a>Debug

Se questo [criterio di sistema](system-policy.md) per computer è impostato su "1", il programma di installazione scrive i messaggi di debug comuni nel debugger usando la funzione [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Se questo valore è impostato su "2", il programma di installazione scrive tutti i messaggi di debug validi nel debugger usando la funzione [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Questo criterio è esclusivamente a scopo di debug e potrebbe non essere supportato nelle versioni future di Windows Installer.

Windows Installer scrive le righe di comando nel file di log solo se il terzo bit (0x04) è impostato nel valore del criterio di debug. Pertanto, per visualizzare le righe di comando nel log, impostare il valore del criterio di debug su 7. Non vengono visualizzate le proprietà associate a un [controllo di modifica](edit-control.md) con l' [attributo di controllo password](password-control-attribute.md). In questo modo le proprietà impostate nella riga di comando saranno visibili nel log anche se la proprietà è inclusa nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) . Per ulteriori informazioni, vedere [impedire che le informazioni riservate vengano scritte nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 
