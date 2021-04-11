---
description: Uso delle classi di base di DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Uso delle classi di base di DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232287"
---
# <a name="using-the-directshow-base-classes"></a>Uso delle classi di base di DirectShow

Per usare le classi di base in DirectShow, è necessario compilare e collegare la libreria di classi di base.

La libreria di classi di base viene fornita come esempio SDK in Microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ). La posizione esatta dipende dalla versione dell'SDK installata, ma dal percorso relativo:

*(Radice degli esempi di SDK)* \\ \\BaseClasses DirectShow

Intestazione: Streams. h

Libreria: nell'esempio vengono compilate le versioni di debug e finale della libreria:

-   Versione definitiva: Strmbase. lib
-   Versione di debug: Strmbasd. lib.

Per ulteriori informazioni sulla configurazione dell'ambiente di compilazione, vedere [configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md).

## <a name="preprocessor-symbols"></a>Simboli del preprocessore

Quando si include il file di intestazione Streams. h, i simboli del preprocessore seguenti hanno un significato speciale:

-   PRESTAZIONI: riservato. Non usare questo simbolo del preprocessore.
-   VFWROBUST: Abilita la convalida del puntatore nella versione finale. Per altre informazioni, vedere [macro Validation Pointer](pointer-validation-macros.md). Nelle build di debug non è necessario definire VFWROBUST.

> [!Note]  
> In Windows Vista e versioni successive, le macro di convalida del puntatore sono vuote.

 

 

 



