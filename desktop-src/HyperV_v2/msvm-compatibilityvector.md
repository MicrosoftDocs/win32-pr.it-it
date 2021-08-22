---
description: Fa riferimento alle informazioni di compatibilità per una macchina virtuale (VM) (se eseguita in un computer vm) o un host (se eseguita in un computer host).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Msvm_CompatibilityVector classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 976e6b7bd9bf69e483b987da4d8055ffc102e89c67ed83bab6aa09c4e586b1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531841"
---
# <a name="msvm_compatibilityvector-class"></a>Classe Msvm \_ CompatibilityVector

Fa riferimento alle informazioni di compatibilità per una macchina virtuale (VM) (se eseguita in un computer vm) o un host (se eseguita in un computer host).

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ CompatibilityVector** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ CompatibilityVector** ha queste proprietà.

<dl> <dt>

**CompareOperation**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica l'operazione di confronto che restituirà true se e solo se due vettori sono compatibili. I dati della macchina virtuale si trova sul lato sinistro del confronto e i dati dell'host si trova sul lato destro.

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

**Uguale** a (0)


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

**Superset** (1)


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

**Subset** (2)


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

**Disgiunto** (3)


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

**GreaterThan** (4)


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

**GreaterThanOrEqual** (5)


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

**LessThan** (6)


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

**LessThanOrEqual** (7)


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

**Multiple** (8)


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

**Divisibile** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**CompatibilityInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati effettivi dell'attributo di compatibilità utilizzati per il confronto.

</dd> <dt>

**VectorId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica un vettore di compatibilità che rappresenta un attributo specifico. Questa proprietà viene usata per trovare la corrispondenza tra i vettori corrispondenti tra un host e una macchina virtuale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il [**metodo GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) della classe [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) restituisce una matrice di istanze **di Msvm \_ CompatibilityVector** per l'host (se eseguito nell'host) o una macchina virtuale (se eseguita nella macchina virtuale). Ogni **voce Msvm \_ CompatibilityVector** nell'elenco descrive un vettore di attributi di compatibilità. Perché una macchina virtuale sia compatibile con un host, tutti gli attributi di compatibilità devono essere compatibili con gli attributi dell'host.

Ogni **voce Msvm \_ CompatibilityVector** ha le proprietà seguenti:

<dl> <dt>

**VectorId**
</dt> <dd>

Identifica in modo univoco il vettore di compatibilità. Viene usato per trovare la corrispondenza con i vettori da confrontare tra un host e una macchina virtuale.

</dd> <dt>

**CompareOperation**
</dt> <dd>

Identifica l'operazione di confronto che determina se i vettori sono compatibili.

</dd> <dt>

**CompatibilityInfo**
</dt> <dd>

Contiene l'attributo di compatibilità effettivo. Si tratta in effetti del payload dell'attributo (ad esempio maschera delle funzionalità del processore, dimensione di scaricamento della riga della cache e così via)

</dd> </dl>

Il set di operazioni definito per **CompareOperation** implica solo il confronto di interi di base e la logica bit per bit. In questo modo il contenuto effettivo **di CompatibilityInfo** rimane opaco. Il set di operazioni include:



| CompareOperation | Descrizione                                      | Confronto di pseudocodice                |
|------------------|--------------------------------------------------|--------------------------------------|
| VmCcEqual        | VmAttr deve essere uguale a HostAttr                       | If (VmAttr == HostAttr)              |
| VmCcSuperSet     | VmAttr deve essere un superset di HostAttr            | If ((VmAttr & HostAttr) == HostAttr) |
| VmCcSubSet       | VmAttr deve essere un subset di HostAttr              | If ((VmAttr & HostAttr) == VmAttr)   |
| VmCcDisjointSet  | VmAttr deve essere un set non contiguo da HostAttr      | If ((VmAttr & HostAttr) == 0)        |
| VmCcGreater      | VmAttr deve essere maggiore di HostAttr             | If (VmAttr > HostAttr)            |
| VmCcGreaterEqual | VmAttr deve essere maggiore o uguale a HostAttr | If (VmAttr >= HostAttr)           |
| VmCcLess         | VmAttr deve essere minore di HostAttr                | If (VmAttr < HostAttr)            |
| VmCcLessEqual    | VmAttr deve essere minore o uguale a HostAttr    | If (VmAttr <= HostAttr)           |
| VmCcMultiple     | VmAttr deve essere un multiplo di HostAttr            | If ((VmAttr % HostAttr) == 0)        |
| VmCcDivisor      | VmAttr deve essere un divisore di HostAttr             | If ((HostAttr % VmAttr) == 0)        |



 

SCVMM deve eseguire questi passaggi per determinare se una macchina virtuale è compatibile con un host.

**Per determinare se una macchina virtuale è compatibile con un host**

1.  Scorrere tutti gli elementi **Msvm \_ CompatibilityVector** per la macchina virtuale.
2.  Per ogni **elemento Msvm \_ CompatibilityVector,** usare l'operazione di compatibilità specificata in **CompareOperation** per confrontare il vettore di compatibilità hardware della macchina virtuale con il vettore di compatibilità corrispondente per l'host.
3.  Se tutti gli elementi **Msvm \_ CompatibilityVector** della macchina virtuale sono considerati compatibili, la macchina virtuale è compatibile con l'host (dal punto di vista della funzionalità del processore).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




