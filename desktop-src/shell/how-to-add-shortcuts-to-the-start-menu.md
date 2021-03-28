---
description: Per aggiungere un elemento al sottomenu programmi, attenersi alla seguente procedura.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Come aggiungere collegamenti al menu Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131630"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a>Come aggiungere collegamenti al menu Start

Per aggiungere un elemento al sottomenu **programmi** , attenersi alla seguente procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare un [collegamento della shell](./links.md) usando l'interfaccia [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .

### <a name="step-2"></a>Passaggio 2:

Ottenere il percorso della cartella programmi usando la funzione [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , passando i [**\_ programmi FOLDERID**](knownfolderid.md).

### <a name="step-3"></a>Passaggio 3:

Aggiungere il collegamento della shell alla cartella programmi. È anche possibile creare una cartella nella cartella programmi e aggiungere il collegamento a tale cartella.

 

 
