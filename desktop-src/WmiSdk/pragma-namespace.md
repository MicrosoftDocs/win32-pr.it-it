---
description: Richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come NamespacePath. Se vengono usati sia l'opzione dello spazio dei nomi del compilatore MOF-n che lo \# spazio dei nomi pragma&\# 32; il comando NamespacePath, il comando ha la priorità sull'opzione.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: spazio dei nomi pragma
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
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753687"
---
# <a name="pragma-namespace"></a>spazio dei nomi pragma

Il comando per il preprocessore **pragma namespace** richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come *namespacePath*. Se vengono usati sia l'opzione dello spazio dei nomi del compilatore MOF **-n** che il comando **\# pragma namespace** *namespacePath* , il comando ha la priorità sull'opzione.

Di seguito viene descritta la sintassi:


```mof
#pragma namespace ("[Namespace]")
```



Lo spazio dei *\[ nomi \]* è lo spazio dei nomi specificato.

Se non si specifica questo comando o l'opzione della riga di comando equivalente, il compilatore MOF utilizzerà lo \\ spazio dei nomi predefinito radice per impostazione predefinita.

## <a name="remarks"></a>Commenti

È possibile richiedere che le applicazioni e gli script client usino una connessione crittografata per l'autenticazione aggiungendo il qualificatore **RequiresEncryption** al file MOF che crea lo spazio dei nomi. È anche possibile modificare uno spazio dei nomi esistente aggiungendo questo attributo e compilare di nuovo il file MOF. Per ulteriori informazioni sull'utilizzo di **RequiresEncryption**, vedere la pagina relativa alla [richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come posizionare le classi o le istanze nello \\ spazio dei nomi "root test".


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

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Qualificatori WMI standard**](standard-wmi-qualifiers.md)
</dt> <dt>

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




