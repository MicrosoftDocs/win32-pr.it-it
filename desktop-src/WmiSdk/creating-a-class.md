---
description: In WMI, una classe è un oggetto che descrive alcuni aspetti di un'azienda, ad esempio un tipo speciale di unità disco.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Creazione di una classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317571"
---
# <a name="creating-a-wmi-class"></a>Creazione di una classe WMI

In WMI, una classe è un oggetto che descrive alcuni aspetti di un'azienda, ad esempio un tipo speciale di unità disco. Dopo aver creato una definizione di classe, scrivere la DLL del provider per fornire le istanze della classe, i dati della proprietà e i metodi Execute definiti per la classe. Gli script e le applicazioni possono quindi ottenere i dati o controllare il dispositivo. Per ulteriori informazioni, vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md).

> [!Note]  
> Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) in caso di errore e riavvio di WMI, utilizzare l'istruzione per il preprocessore dell'istruzione [**\# pragma autocover**](pragma-autorecover.md) nel file MOF.

 

## <a name="base-class"></a>Classe di base

Una classe di base rappresenta un concetto generale. Ad esempio, la classe [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) rappresenta tutti i tipi di unità CD-ROM in WMI e contiene le proprietà generali che descrivono tutti i tipi di unità CD-ROM. Per ulteriori informazioni, vedere [creazione di una classe di base](creating-a-base-class.md).

Una classe derivata eredita proprietà e metodi da un'altra classe. Una classe derivata rappresenta in genere un caso specifico di una classe base. Ad esempio, la classe [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) rappresenta un'unità CD-ROM in un sistema Windows. La classe **Win32 \_ CDROMDrive** è basata su e eredita molte proprietà da [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive). Tuttavia, **\_ CDROMDrive Win32**, come altre classi derivate, possono avere proprietà aggiuntive che rendono univoca la classe derivata. Per ulteriori informazioni, vedere [creazione di una classe derivata](creating-a-derived-class.md).

## <a name="properties-and-methods"></a>Proprietà e metodi

La creazione di una classe significa definire le proprietà che descrivono tale classe. È anche possibile definire metodi che modificano l'oggetto rappresentato dalla classe.

In genere, una proprietà rappresenta un aspetto dell'oggetto, ad esempio un numero di serie per un dispositivo o una dimensione in byte per un processo, mentre un metodo rappresenta un'azione che modifica lo stato o il comportamento del dispositivo o dell'entità logica.

Ogni classe deve avere almeno una proprietà chiave. Mentre una classe può avere più chiavi, non è possibile creare un'istanza di una classe con più di 256 di chiavi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
