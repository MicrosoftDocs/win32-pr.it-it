---
description: I file binari di Windows Server 2003 con Service Pack 1 (SP1) sono compatibili con Windows Vista e Windows Server 2008. È tuttavia necessario ricompilare i file binari di versioni precedenti di Windows.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Porting di applicazioni di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528710"
---
# <a name="porting-backup-applications"></a>Porting di applicazioni di backup

I file binari di Windows Server 2003 con Service Pack 1 (SP1) sono compatibili con Windows Vista e Windows Server 2008. È tuttavia necessario ricompilare i file binari di versioni precedenti di Windows.

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>Porting di applicazioni di backup Windows XP a Windows Vista

Diverse interfacce VSS sono state modificate rispetto a Windows XP. Come minimo, le applicazioni Windows XP devono essere ricompilate utilizzando i file di intestazione e le librerie di VSS 7,2 SDK o Windows Vista o Windows Server 2008 SDK.

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>Porting di applicazioni di backup di Windows Server 2003 SP1 a Windows Vista

I file binari di Windows Server 2003 con SP1 sono compatibili con Windows Vista e Windows Server 2008. Tuttavia, la maggior parte delle applicazioni di backup di Windows Server 2003 con SP1 deve essere aggiornata per tenere conto di nuove funzionalità, descritte nelle sezioni seguenti.

## <a name="compiling-backup-applications-for-windows-vista"></a>Compilazione di applicazioni di backup per Windows Vista

Le applicazioni che usano le interfacce disponibili in Windows Server 2003 possono essere compilate usando i file di intestazione e le librerie fornite in VSS 7,2 SDK. Per utilizzare le nuove interfacce, è necessario ricompilare le applicazioni utilizzando i file di intestazione e le librerie incluse in Windows Vista SDK.

> [!Note]  
> I file binari compilati con Windows Vista o Windows Server 2008 non sono compatibili con Windows Server 2003 con SP1 o versioni precedenti di Windows.

 

 

 



