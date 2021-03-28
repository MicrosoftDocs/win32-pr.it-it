---
description: "Un'altra opzione per l'aggiunta di verbi a un menu a cascata consiste nell'usare IExplorerCommand:: EnumSubCommands."
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Creare menu a cascata con l'interfaccia IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104550997"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Come creare menu a cascata con l'interfaccia IExplorerCommand

Un'altra opzione per l'aggiunta di verbi a un menu a cascata consiste nell'usare [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Questo metodo consente alle origini dati che forniscono i comandi del modulo di comando tramite l'interfaccia [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) di utilizzare tali comandi come verbi in un menu di scelta rapida. In Windows 7 e versioni successive, è possibile fornire la stessa implementazione del verbo usando l'interfaccia [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , come è possibile con l'interfaccia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .

## <a name="instructions"></a>Istruzioni


Le due schermate seguenti illustrano l'uso dei menu a cascata nella cartella **Devices** .

![Screenshot che mostra un esempio di menu a cascata nella cartella Devices (dispositivi).](images/file-assoc/filecascademenu.png)

![screenshot che mostra un esempio di menu a cascata nella cartella Devices](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a>Commenti

> [!Note]  
> Poiché [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supporta solo l'attivazione in-process, è consigliabile usare le origini dati della shell che devono condividere l'implementazione tra i comandi e i menu di scelta rapida.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
