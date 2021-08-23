---
description: Gli sviluppatori possono estendere l'infrastruttura WMI sviluppando provider WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Creazione di provider WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cb15b911cb549e28e3536da0a9da31de8df1d6f395ede5f9c9176d21239abc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679741"
---
# <a name="creating-wmi-providers"></a>Creazione di provider WMI

Gli sviluppatori possono estendere l'infrastruttura WMI sviluppando provider WMI. I provider WMI sono oggetti COM che implementano un set specificato di interfacce e, fino a poco tempo fa, sono sempre stati implementati in C++. È ora possibile usare linguaggi gestiti come C# per implementare provider WMI. Nella versione 3.5 di .NET Framework è stato introdotto il framework delle estensioni del provider WMI che rende possibile questa operazione. Per altre informazioni sulla creazione di provider WMI usando tale framework, leggere l'articolo Scrittura di provider WMI accoppiati con WMI.NET [Provider Extension 2.0.](/previous-versions/dotnet/articles/cc268228(v=msdn.10))

> [!Note]  
> È anche possibile creare un provider usando Windows Management Infrastructure (MI), la versione di nuova generazione di WMI. Per altre informazioni, vedere [How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

Nella tabella seguente viene descritto il contenuto di questa sezione.



| Argomento                                                      | Descrizione                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Fornire dati a WMI](providing-data-to-wmi.md)         | Viene fornita una panoramica dei passaggi necessari per la creazione di un provider WMI.         |
| [Sviluppo di un provider WMI](developing-a-wmi-provider.md) | Vengono descritte le attività che è necessario eseguire durante la creazione di vari tipi di provider WMI. |



 

 

 
