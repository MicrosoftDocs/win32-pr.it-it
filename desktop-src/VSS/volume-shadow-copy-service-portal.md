---
description: Eseguire il backup dei volumi mentre le applicazioni in un sistema continuano a scrivere nei volumi. Ridurre al minimo i tempi di inattività dell'applicazione creando rapidamente uno snapshot (copia shadow) di un volume che duplica tutti i dati. Eseguire il backup multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307172"
---
# <a name="volume-shadow-copy-service"></a>Servizio Copia Shadow del volume

## <a name="purpose"></a>Scopo

Il Servizio Copia Shadow del volume (VSS) è un set di interfacce COM che implementa un Framework per consentire l'esecuzione dei backup del volume mentre le applicazioni in un sistema continuano a scrivere nei volumi.

Per un'introduzione a VSS per gli amministratori di sistema, vedere [servizio Copia Shadow del volume](/windows-server/storage/file-server/volume-shadow-copy-service) nella libreria TechNet.

## <a name="run-time-requirements"></a>Requisiti di runtime

VSS è supportato in Microsoft Windows XP e versioni successive. Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della documentazione relativa a tale elemento.

Tutte le applicazioni VSS a 32 bit, ovvero i richiedenti, i provider e i writer, devono essere eseguite come applicazioni native a 32 bit o 64 bit. L'esecuzione in WOW64 non è supportata. Per ulteriori informazioni, vedere [configurazioni e restrizioni supportate](usage-conventions.md).

**Windows Server 2003 e Windows XP:** L'esecuzione di richiedenti VSS a 32 bit in WOW64 è supportata, ma non per i backup dello stato del sistema. L'esecuzione di provider e writer VSS a 32 bit in WOW64 non è supportata. Il supporto per l'esecuzione di richiedenti a 32 bit in WOW64 è stato rimosso in Windows Vista e nelle versioni successive.

> [!Note]  
> Non è possibile usare una copia shadow creata in Windows Server 2003 R2 o Windows Server 2003 in un computer che esegue Windows Server 2008 R2 o Windows Server 2008. Non è possibile usare una copia shadow creata in Windows Server 2008 R2 o Windows Server 2008 in un computer che esegue Windows Server 2003. Tuttavia, una copia shadow creata in Windows Server 2008 può essere usata in un computer che esegue Windows Server 2008 R2 e viceversa.

 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                          | Descrizione                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Overview](volume-shadow-copy-service-overview.md)<br/> | Descrive il modello a oggetti VSS, le strategie di backup e ripristino e come creare provider VSS, richiedenti e writer.<br/> |
| [Riferimento](volume-shadow-copy-reference.md)<br/>       | Descrive le classi VSS, i tipi di dati, le enumerazioni, le funzioni, le interfacce e le strutture.<br/>                                  |



 

## <a name="additional-resources"></a>Risorse aggiuntive



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista e versioni successive            | VSS è disponibile nel Software Development Kit (SDK) di Microsoft Windows. È possibile installare l'SDK per Windows 7 e Windows Server 2008 R2 dall' [area download di Windows](https://www.microsoft.com/download/details.aspx?id=8279). È anche possibile scaricare la [versione ISO](https://www.microsoft.com/download/details.aspx?id=8442) dell'SDK dall'area download di Windows. Le versioni precedenti dell'SDK possono essere scaricate dalla [pagina di Download Windows SDK](https://msdn.microsoft.com/windows/bb980924.aspx). |
| Windows Server 2003 e Windows XP | VSS è disponibile nell'SDK Servizio Copia Shadow del volume 7,2, che è possibile scaricare dall' [area download di Windows](https://www.microsoft.com/download/details.aspx?id=23490). Si noti che i file vssapi. lib a 64 bit nelle directory sotto la \\ directory Win2003 obj possono essere usati per le versioni a 64 bit di Windows Server 2003 e Windows XP.                                                                                                                                                                 |



 

 

 
