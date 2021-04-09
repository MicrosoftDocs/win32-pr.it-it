---
description: Gli sviluppatori possono estendere l'infrastruttura WMI sviluppando provider WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Creazione di provider WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058345"
---
# <a name="creating-wmi-providers"></a>Creazione di provider WMI

Gli sviluppatori possono estendere l'infrastruttura WMI sviluppando provider WMI. I provider WMI sono oggetti COM che implementano un set specificato di interfacce e, fino a poco tempo, sono sempre implementate in C++. È ora possibile utilizzare linguaggi gestiti come C# per implementare i provider WMI. La versione 3,5 di .NET Framework ha introdotto il framework delle estensioni del provider WMI che lo rende possibile. Per ulteriori informazioni sulla creazione di provider WMI mediante tale Framework, vedere l'articolo relativo alla [scrittura di provider WMI associati mediante l'estensione WMI.NET del Provider 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> È inoltre possibile creare un provider utilizzando Windows Management Infrastructure (MI), la versione di nuova generazione di WMI. Per ulteriori informazioni, vedere [How to implement a mi provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

Nella tabella seguente viene descritto il contenuto di questa sezione.



| Argomento                                                      | Descrizione                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Invio di dati a WMI](providing-data-to-wmi.md)         | Viene fornita una panoramica dei passaggi necessari per la creazione di un provider WMI.         |
| [Sviluppo di un provider WMI](developing-a-wmi-provider.md) | Descrive le attività che è necessario eseguire durante la creazione di diversi tipi di provider WMI. |



 

 

 
