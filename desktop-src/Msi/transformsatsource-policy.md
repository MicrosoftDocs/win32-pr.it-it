---
description: Se il criterio di sistema per utente è impostato su &\# 0034; 1&\# 0034;, il programma di installazione cerca i file di trasformazione nella radice di tutte le origini di rete nell'elenco di origine per il prodotto. Per impostazione predefinita, le trasformazioni vengono archiviate nella cartella Application Data del profilo di un utente.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Criteri di TransformsAtSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128107"
---
# <a name="transformsatsource-policy"></a>Criteri di TransformsAtSource

Se il [criterio di sistema](system-policy.md) per utente è impostato su "1"; il programma di installazione cerca i file di trasformazione nella radice di qualsiasi origine di rete nell'elenco di origine per il prodotto. Per impostazione predefinita, le trasformazioni vengono archiviate nella cartella Application Data del profilo di un utente.

Windows Installer interpreta il criterio TransformsAtSource in modo che corrisponda al [criterio TRANSFORMSSECURE](transformssecure-policy.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ SZ**

 

 



