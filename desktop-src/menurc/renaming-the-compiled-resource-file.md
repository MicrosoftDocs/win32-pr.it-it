---
title: Ridenominazione del file di risorse compilato
description: Per impostazione predefinita, durante la compilazione delle risorse, RC denota il file di risorse compilato (con estensione res) con il nome di base del file RC e lo inserisce nella stessa directory del file RC.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f2a920eeed6c1b96b512511b965b0243b89e4f6888120c6183b7a3104963c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733518"
---
# <a name="renaming-the-compiled-resource-file"></a>Ridenominazione del file di risorse compilato

Per impostazione predefinita, durante la compilazione delle risorse, RC denota il file di risorse compilato (con estensione res) con il nome di base del file RC e lo inserisce nella stessa directory del file RC. CvTRES deve quindi essere richiamato per convertire il file con estensione res in un formato di risorsa binaria (con estensione rbj) che può essere riconosciuto dal linker. L'esempio seguente compila MyApp.rc e crea un file di risorse compilato denominato MyApp.res nella stessa directory di MyApp.rc:

**rc myapp.rc**

**L'opzione /fo** assegna al file res risultante un nome diverso dal nome del file RC corrispondente. Ad esempio, per assegnare al file res risultante il nome NewFile.res, usare il comando seguente:

**rc -fo newfile.res myapp.rc**

**L'opzione /fo** può anche inserire il file con estensione res in una directory diversa. Ad esempio, il comando seguente inserisce il file di risorse compilato MyApp.res nella directory C: \\ Risorsa di \\ origine:

**rc -fo c: \\ risorsa \\ di origine \\ myapp.res myapp.rc**

 

 




