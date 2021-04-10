---
description: I contesti di applicazione possono essere usati per creare classi di Windows affiancate.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Creazione di classi di Windows affiancate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882666"
---
# <a name="creating-side-by-side-windows-classes"></a>Creazione di classi di Windows affiancate

I contesti di applicazione possono essere usati per creare classi di Windows affiancate. Con le classi Windows affiancate, l'applicazione può avere versioni diverse di una classe attiva contemporaneamente in una finestra padre solitaria. Per creare una classe Windows affiancata, l'applicazione deve attivare un contesto di attivazione prima di chiamare [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per ottenere un handle per la nuova finestra.

I controlli comuni di Windows versione 5,82 e la versione 6,0 hanno ad esempio un controllo di modifica. Per impostazione predefinita, Windows utilizza il controllo di modifica della versione 5,82. Per ottenere una finestra affiancata con il controllo di modifica della versione 6,0, prima di chiamare [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) come di consueto, l'applicazione può fare riferimento a un assembly che espone le classi finestra denominate e quindi attivare il contesto di attivazione che fa riferimento ai controlli della versione 6,0.

 

 
