---
description: 'Altre informazioni su: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee83dc86aa6faf5fab0b45596a586c657e4c6e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474127"
---
# <a name="jet_snp"></a>JET_SNP


_**Si applica a:** Windows | Windows Server_

## <a name="jet_snp"></a>JET_SNP

Il **JET_SNP** di costanti descrive il tipo di operazione per cui devono essere ottenute le informazioni sullo stato di avanzamento. Queste costanti vengono usate come parametro *snp* della funzione [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback.


| <p>Costante/valore</p> | <p>Descrizione</p> | 
|-----------------------|--------------------|
| <p>JET_snpRepair<br />2</p> | <p>Il callback è per un'operazione di ripristino.</p> | 
| <p>JET_snpCompact<br />4</p> | <p>Il callback è per la deframmentazione del database.</p> | 
| <p>JET_snpRestore<br />8</p> | <p>Il callback è per un'operazione di ripristino.</p> | 
| <p>JET_snpBackup<br />9</p> | <p>Il callback è per un'operazione di backup.</p> | 
| <p>JET_snpUpgrade<br />10</p> | <p>Non supportata.</p><p><strong>Windows 2000:</strong>  Il callback è per l'operazione di aggiornamento del formato del database.</p> | 
| <p>JET_snpScrub<br />11</p> | <p>Il callback è per un'operazione di azzeramento del database (ovvero pulitura).</p><p><strong>Windows Server 2003 e Windows 2000 Server:</strong>  Non supportato.</p> | 
| <p>JET_snpUpgradeRecordFormat<br />12</p> | <p>Il callback è per il processo di aggiornamento del formato di record di tutte le pagine del database.</p><p><strong>Windows Server 2003 e Windows 2000 Server:</strong>  Non supportato.</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
