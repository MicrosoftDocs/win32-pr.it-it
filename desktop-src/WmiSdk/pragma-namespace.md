---
description: Richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come namespacepath. Se vengono usati sia l'opzione del compilatore MOF -n dello spazio dei nomi che il comando \# pragma namespace&32;namespacepath, il comando ha la priorità \# sull'opzione .
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: Spazio dei nomi pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3eea58c8e32ab8b1b851205b365b837194d0472a1c39017e2eb69dc3fe70a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316827"
---
# <a name="pragma-namespace"></a>Spazio dei nomi pragma

Il **comando per** il preprocessore dello spazio dei nomi pragma richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come *namespacepath*. Se vengono usati sia l'opzione del compilatore MOF **-n** dello spazio dei nomi che il comando **\# pragma namespace** *namespacepath,* il comando ha la priorità sull'opzione .

Di seguito viene descritta la sintassi:


```mof
#pragma namespace ("[Namespace]")
```



*\[ Lo \] spazio* dei nomi è lo spazio dei nomi specificato.

Se non si specifica questo comando o l'opzione della riga di comando equivalente, il compilatore MOF usa lo spazio dei nomi predefinito radice \\ per impostazione predefinita.

## <a name="remarks"></a>Commenti

È possibile richiedere che gli script client e le applicazioni usino una connessione crittografata per l'autenticazione aggiungendo il qualificatore **RequiresEncryption** al file mof che crea lo spazio dei nomi. È anche possibile modificare uno spazio dei nomi esistente aggiungendo questo attributo e compilare nuovamente il file MOF. Per altre informazioni su come usare **RequiresEncryption,** vedere Richiesta di una [connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra come inserire classi o istanze nello spazio dei nomi "Root \\ Test".


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Impostazione dei descrittori di sicurezza di Namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Qualificatori WMI standard**](standard-wmi-qualifiers.md)
</dt> <dt>

[Comandi per il preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




