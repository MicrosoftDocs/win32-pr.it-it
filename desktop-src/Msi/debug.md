---
description: Se questo criterio di sistema per computer è impostato su &\# 0034;1&0034;, il programma di installazione scrive messaggi di debug comuni nel debugger usando la funzione \# OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3216b863953faa7edf3f8146084a0ec794f171482e0e619d717447ca0a0f30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692871"
---
# <a name="debug"></a>Debug

Se questo criterio di [sistema](system-policy.md) per computer è impostato su "1", il programma di installazione scrive messaggi di debug comuni nel debugger usando la [**funzione OutputDebugString.**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Se questo valore è impostato su "2", il programma di installazione scrive tutti i messaggi di debug validi nel debugger usando la [**funzione OutputDebugString.**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Questo criterio è solo a scopo di debug e potrebbe non essere supportato nelle versioni future Windows Programma di installazione.

Windows Il programma di installazione scrive le righe di comando nel file di log solo se il terzo bit (0x04) è impostato nel valore dei criteri di debug. Pertanto, per visualizzare le righe di comando nel log, impostare il valore dei criteri debug su 7. In questo modo non vengono visualizzate le proprietà associate a [un controllo di modifica con](edit-control.md) l'attributo del controllo [password](password-control-attribute.md). In questo modo le proprietà impostate nella riga di comando saranno visibili nel log anche se la proprietà è inclusa nella [**proprietà MsiHiddenProperties.**](msihiddenproperties.md) Per altre informazioni, vedere [Preventing Confidential Information From Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione \\  \\ **Windows** \\ **Microsoft**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 
