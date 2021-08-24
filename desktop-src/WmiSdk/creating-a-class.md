---
description: In WMI una classe è un oggetto che descrive alcuni aspetti di un'azienda, ad esempio un tipo speciale di unità disco.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Creazione di una classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2db62f1f0d14035f7bcc3fd74f8bbbfbacf08cb0dbf139b06c9870b7039e19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612561"
---
# <a name="creating-a-wmi-class"></a>Creazione di una classe WMI

In WMI una classe è un oggetto che descrive alcuni aspetti di un'azienda, ad esempio un tipo speciale di unità disco. Dopo aver creato una definizione di classe, scrivere la DLL del provider per fornire le istanze della classe, i dati delle proprietà e i metodi di esecuzione definiti per la classe. Gli script e le applicazioni possono quindi ottenere dati o controllare il dispositivo. Per altre informazioni, vedere [Sviluppo di un provider WMI.](developing-a-wmi-provider.md)

> [!Note]  
> Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti siano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e si riavvia, usare l'istruzione del preprocessore [**\# pragma autorecover**](pragma-autorecover.md) nel file MOF.

 

## <a name="base-class"></a>Classe di base

Una classe di base rappresenta un concetto generale. Ad esempio, la [**classe \_ CIM CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) rappresenta tutti i tipi di unità CD-ROM in WMI e contiene proprietà generali che descrivono tutti i tipi di unità CD-ROM. Per altre informazioni, vedere [Creazione di una classe base.](creating-a-base-class.md)

Una classe derivata eredita proprietà e metodi da un'altra classe. Una classe derivata rappresenta in genere un caso specifico di una classe di base. Ad esempio, la [**classe WIN32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) rappresenta un'unità CD-ROM in un Windows sistema. La **classe WIN32 \_ CDROMDrive** si basa su ed eredita molte proprietà da [**CIM \_ CDROMDrive.**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) Tuttavia, **\_ CdROMDrive Win32,** come altre classi derivate, può avere proprietà aggiuntive che rendono univoca la classe derivata. Per altre informazioni, vedere [Creazione di una classe derivata.](creating-a-derived-class.md)

## <a name="properties-and-methods"></a>Proprietà e metodi

La creazione di una classe implica la definizione delle proprietà che descrivono tale classe. È anche possibile definire metodi che modificano l'oggetto rappresentato dalla classe .

In genere, una proprietà rappresenta un aspetto dell'oggetto, ad esempio un numero di serie per un dispositivo o una dimensione in byte per un processo, mentre un metodo rappresenta un'azione che modifica lo stato o il comportamento del dispositivo o dell'entità logica.

Ogni classe deve avere almeno una proprietà chiave. Sebbene una classe possa avere più chiavi, non è possibile creare un'istanza di una classe con più di 256 chiavi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
