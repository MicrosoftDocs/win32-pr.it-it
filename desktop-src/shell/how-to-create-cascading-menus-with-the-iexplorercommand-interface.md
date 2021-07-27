---
description: Un'altra opzione per aggiungere verbi a un menu a cascata è tramite IExplorerCommand::EnumSubCommands.
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Creare menu a cascata con l'interfaccia IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed12cf78dc4b5f6a77bbd00b06897b49474a401
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436096"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Come creare menu a cascata con l'interfaccia IExplorerCommand

Un'altra opzione per aggiungere verbi a un menu a cascata è [**tramite IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Questo metodo consente alle origini dati che forniscono i comandi del modulo comandi tramite [**l'interfaccia IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) di usare tali comandi come verbi in un menu di scelta rapida. In Windows 7 e versioni successive è possibile fornire la stessa implementazione del verbo usando l'interfaccia [**IExplorerCommand,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) come è possibile fare con [**l'interfaccia IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)

## <a name="instructions"></a>Istruzioni


Le due schermate seguenti illustrano l'uso dei menu a cascata nella **cartella** Dispositivi.

![Screenshot che mostra un esempio di menu a cascata nella cartella devices.](images/file-assoc/FileCascadeMenu.png)

![Screenshot che mostra un esempio di menu a cascata nella cartella devices](images/file-assoc/cascadeDevices2.png)

## <a name="remarks"></a>Commenti

> [!Note]  
> Poiché [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supporta solo l'attivazione in-process, è consigliabile usarlo dalle origini dati della shell che devono condividere l'implementazione tra comandi e menu di scelta rapida.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
