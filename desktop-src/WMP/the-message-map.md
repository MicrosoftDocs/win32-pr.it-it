---
title: Mappa messaggi
description: Mappa messaggi
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Plug-in di Windows Media Player, mappa messaggi
- plug-in, mappa messaggi
- plug-in dell'interfaccia utente, mappa messaggi
- Plug-in dell'interfaccia utente, mappa messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044824"
---
# <a name="the-message-map"></a>Mappa messaggi

La finestra del plug-in risponde a vari eventi chiamando metodi mappati ai messaggi di evento corrispondenti. La procedura guidata fornisce un mapping affinché OnPaint e OnEraseBackground vengano chiamati nei momenti appropriati. Per creare il pulsante **Cerca** e rispondere ai clic, la sezione della mappa messaggi viene modificata come segue:


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




