---
title: Estensione delle funzioni OpenGL
description: La libreria OpenGL supporta più implementazioni delle relative funzioni.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL in Windows,funzioni di estensione
- Funzioni di estensione OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dce68498d5a3e672e63da1ae05d9bb513a4121d110237d90cdad75df0ff84d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361343"
---
# <a name="extending-opengl-functions"></a>Estensione delle funzioni OpenGL

La libreria OpenGL supporta più implementazioni delle relative funzioni. Le funzioni di estensione supportate in un contesto di rendering non sono necessariamente supportate in un contesto di rendering diverso. Per un determinato contesto di rendering in un'applicazione che usa funzioni di estensione, usare solo gli indirizzi di funzione restituiti dalla [**funzione wglGetProcAddress.**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)

 

 




