---
description: Se questo criterio di sistema per utente è impostato su &\# 0034;1&0034;, il programma di installazione cerca i file di trasformazione nella radice di qualsiasi origine di rete nell'elenco di origine per il \# prodotto. Per impostazione predefinita, le trasformazioni vengono archiviate nella cartella Dati applicazione del profilo di un utente.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Criteri TransformsAtSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab909fd728ce1cebba894dd8598879fa055ce762ed027cd8842cc7236a0f24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623480"
---
# <a name="transformsatsource-policy"></a>Criteri TransformsAtSource

Se questo criterio di sistema [per utente](system-policy.md) è impostato su "1"; il programma di installazione cerca i file di trasformazione nella radice di qualsiasi origine di rete nell'elenco di origine per il prodotto. Per impostazione predefinita, le trasformazioni vengono archiviate nella cartella Dati applicazione del profilo di un utente.

Windows Il programma di installazione interpreta i criteri TransformsAtSource come i [criteri TransformsSecure.](transformssecure-policy.md)

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ SZ**

 

 



