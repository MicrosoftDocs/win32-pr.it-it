---
title: Icone (menu e altre risorse)
description: In questa sezione vengono descritte le icone che sono immagini bitmap combinate con una maschera per creare aree trasparenti nell'immagine.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\icons.htm
keywords:
- risorse, icone
- icone, informazioni
- Risorsa RT_ICON
- Risorsa RT_GROUP_ICON
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c96e740c23bb61cfdaa6cfbcbf6d0ce7538586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400169"
---
# <a name="icons-menus-and-other-resources"></a>Icone (menu e altre risorse)

Un' *icona* è un'immagine costituita da un'immagine bitmap combinata con una maschera per creare aree trasparenti nell'immagine. Il termine icona può fare riferimento a uno dei seguenti elementi:

-   Immagine A icona singola. Si tratta di una risorsa di tipo **RT \_ Icon**.
-   Un gruppo di immagini, da cui il sistema o un'applicazione può scegliere l'icona più appropriata in base alle dimensioni e alla profondità dei colori. Si tratta di una risorsa di **tipo \_ \_ icona del gruppo RT**.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                 | Descrizione                                                 |
|--------------------------------------|-------------------------------------------------------------|
| [Informazioni sulle icone](about-icons.md)       | Vengono illustrate le icone.<br/>                                 |
| [Uso delle icone](using-icons.md)       | Viene illustrato come eseguire attività correlate alle icone.<br/> |
| [Riferimento icona](icon-reference.md) | Contiene il riferimento all'API.<br/>                      |



 

### <a name="icon-functions"></a>Funzioni icona



| Nome                                                               | Descrizione                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon)                                       | Copia l'icona specificata da un altro modulo al modulo corrente. <br/>                                                                                                                                      |
| [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon)                                   | Crea un'icona con le dimensioni, i colori e gli schemi di bit specificati. <br/>                                                                                                                                    |
| [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)           | Crea un'icona o un cursore da bit di risorsa che descrivono l'icona.<br/>                                                                                                                                          |
| [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)       | Crea un'icona o un cursore da bit di risorsa che descrivono l'icona. <br/>                                                                                                                                         |
| [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)                   | Crea un'icona o un cursore da una struttura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . <br/>                                                                                                                                 |
| [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                 | Elimina un'icona e libera la memoria occupata dall'icona. <br/>                                                                                                                                                  |
| [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)                                       | Disegna un'icona o un cursore nel contesto di dispositivo specificato.<br/>                                                                                                                                                 |
| [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex)                                   | Disegna un'icona o un cursore nel contesto di dispositivo specificato, eseguendo le operazioni raster specificate e allungando o comprimendo l'icona o il cursore come specificato. <br/>                                     |
| [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon)                             | Crea un duplicato di un'icona specificata.<br/>                                                                                                                                                                   |
| [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)             | Recupera un handle per un'icona indicizzata trovata in un file o un'icona trovata in un file eseguibile associato. <br/>                                                                                                  |
| [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)                                 | Recupera un handle per un'icona dal file eseguibile, dalla DLL o dal file di icona specificati.<br/>                                                                                                                        |
| [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)                             | Crea una matrice di handle per icone grandi o piccole estratte dal file eseguibile, dalla DLL o dal file di icona specificato. <br/>                                                                                      |
| [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)                                 | Recupera le informazioni sull'icona o sul cursore specificato. <br/>                                                                                                                                                 |
| [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)                             | Recupera le informazioni sull'icona o sul cursore specificato. [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa) estende [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) usando la struttura [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa) più recente.<br/> |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                                       | Carica la risorsa icona specificata dal file eseguibile (exe) associato a un'istanza dell'applicazione.<br/>                                                                                                 |
| [**LookupIconIdFromDirectory**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectory)     | Cerca nell'icona o nel cursore i dati del cursore più adatti al dispositivo di visualizzazione corrente.<br/>                                                                                                     |
| [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) | Cerca nell'icona o nel cursore i dati del cursore più adatti al dispositivo di visualizzazione corrente. <br/>                                                                                                    |
| [**PrivateExtractIcons**](/windows/desktop/api/Winuser/nf-winuser-privateextracticonsa)                 | Crea una matrice di handle per le icone estratte da un file specificato.<br/>                                                                                                                             |



 

### <a name="icon-structures"></a>Strutture delle icone



| Nome                               | Descrizione                                                                                                                                                                                                                                     |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo)       | Contiene informazioni su un'icona o un cursore. <br/>                                                                                                                                                                                     |
| [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa)   | Contiene informazioni su un'icona o un cursore. Estende [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo). Usato da [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa).<br/>                                                                                                |
| [**ICONMETRICS**](/windows/win32/api/winuser/ns-winuser-iconmetricsa) | Contiene le metriche scalabili associate alle icone. Questa struttura viene utilizzata con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) quando si specifica l'azione **SPI \_ GETICONMETRICS** o **SPI \_ SETICONMETRICS** .<br/> |



 

 

