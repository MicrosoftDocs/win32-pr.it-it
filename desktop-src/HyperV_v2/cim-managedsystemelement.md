---
description: CIM \_ ManagedSystemElement è la classe di base per la gerarchia degli elementi di sistema. Qualsiasi componente di un sistema può essere potenzialmente rappresentato da questa classe o dalle relative sottoclassi.
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: CIM_ManagedSystemElement classe (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0056aa172827bde2967c20c1f8b8922c2bfcb5165adc4e03d94c98f30748157e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812018"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a>CIM_ManagedSystemElement classe (gestione Hyper-V)

**CIM \_ ManagedSystemElement è** la classe di base per la gerarchia degli elementi di sistema. Qualsiasi componente di un sistema può essere potenzialmente rappresentato da questa classe o dalle relative sottoclassi.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
};
```

## <a name="members"></a>Members

La **classe CIM \_ ManagedSystemElement** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ManagedSystemElement** ha queste proprietà.

<dl> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la possibilità della strumentazione di comunicare con questo elemento. Un **valore NULL** indica che la strumentazione non supporta questa proprietà.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

**Non disponibile** (1)


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

**Comunicazione OK** (2)


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

**Comunicazione persa** (3)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (0x8000.)


</dt> <dd></dd> </dl>

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**", "**CIM \_ ManagedSystemElement**.**HealthState**")
</dt> </dl>

Indica dettagli aggiuntivi sullo stato che completano la **proprietà PrimaryStatus.** Un **valore NULL** indica che la strumentazione non supporta questa proprietà.

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

**Non disponibile** (0)


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

**Nessuna informazione aggiuntiva** (1)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressato** (2)


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

**Errore predittivo** (3)


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

**Errore non ripristinabile** (4)


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

**Entità di supporto in errore** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (0x8000.)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'integrità corrente dell'elemento. Questo attributo esprime l'integrità di questo elemento, ma non necessariamente l'integrità dei relativi sottocomponenti.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (5)


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

**Danneggiato/Avviso** (10)


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

**Errore secondario** (15)


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

**Errore principale** (20)


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

**Errore critico** (25)


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

**Errore non ripristinabile** (30)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Etichetta con cui l'oggetto è noto. In caso di sottoclasse, la **proprietà Name** può essere sottoposta a override per essere una proprietà chiave.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")
</dt> </dl>

Indica la condizione operativa corrente dell'elemento. Questa proprietà può essere usata per fornire informazioni più dettagliate sul valore della **proprietà EnabledState.** Un **valore NULL** indica che la strumentazione non supporta questa proprietà.

"Sconosciuto" indica

"None" indica che

"Manutenzione"

"Avvio"

"Arresto"

"Stopped" e "Aborted" sono simili, anche se il primo , mentre il secondo i

"Dormant" indica che

"Completed" indica che t

"Migrazione"

"Disasserazione"

"Emigrazione"

"Arresto in fase di arresto"

"In test"

"Transizione"

"In servizio"

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

L'implementazione è in genere in grado di restituire questa proprietà, ma non è in grado di eseguire questa operazione in questo momento.

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)


</dt> <dd>

L'implementazione (provider) è in grado di restituire un valore per questa proprietà, ma non mai per questo particolare componente hardware/software o la proprietà non viene intenzionalmente usata perché non aggiunge informazioni significative (come nel caso di una proprietà destinata ad aggiungere altre informazioni a un'altra proprietà).

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)


</dt> <dd>

Descrive un elemento configurato, gestito, pulito o amministrato in altro modo.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A partire** da (3)


</dt> <dd>

Descrive un elemento in fase di inizializzazione.

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** (4)


</dt> <dd>

Descrive un elemento che viene portato a un arresto ordinato.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)


</dt> <dd>

Si è verificata un'interruzione pulita e ordinata.

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)


</dt> <dd>

Si è verificata un'arresto improvviso, in cui potrebbe essere necessario aggiornare lo stato e la configurazione dell'elemento.

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattiva** (7)


</dt> <dd>

L'elemento è inattivo o inattivo.

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)


</dt> <dd>

L'elemento ha completato l'operazione. Questo valore deve essere combinato con OK, Error o Degraded in PrimaryStatus in modo che un client possa determinare se l'operazione completa è stata completata con OK (superato), Completato con errore (operazione non riuscita) o Completato con danneggiato (l'operazione è stata completata, ma non è stata completata o non ha riportato un errore).

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)


</dt> <dd>

L'elemento viene spostato tra gli elementi host.

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Ing** (10)


</dt> <dd>

L'elemento viene spostato dall'elemento host.

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Cheng** (11)


</dt> <dd>

L'elemento viene spostato in un nuovo elemento host.

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Creazione di snapshot** (12)


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto in fase di** arresto (13)


</dt> <dd>

Descrive un elemento che viene portato a un arresto improvviso.

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)


</dt> <dd>

L'elemento esegue funzioni di test.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)


</dt> <dd>

Descrive un elemento che si trova tra gli stati, ad esempio non è completamente disponibile né nello stato precedente né nello stato successivo. Questo valore deve essere usato se non sono applicabili altri valori che indicano una transizione a uno stato specifico.

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In servizio** (16)


</dt> <dd>

Descrive un elemento in servizio e operativo.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (0x8000.)


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**StatusDescriptions**")
</dt> </dl>

Contiene indicatori dello stato corrente dell'elemento. Il primo valore della proprietà **OperationalStatus** deve contenere lo stato primario per l'elemento .

> [!Note]  
> La **proprietà OperationalStatus** sostituisce la proprietà **Status** deprecata. A causa dell'uso diffuso della proprietà **Status** esistente nelle applicazioni di gestione, è consigliabile che i provider o la strumentazione forniranno entrambe le **proprietà Status** **e OperationalStatus.** Quando instrumentato, **Status**, poiché si tratta di una proprietà a valore singolo, deve fornire anche lo stato primario dell'elemento.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**OK** (2)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (3)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (4)


</dt> <dd>

L'elemento funziona, ma richiede attenzione. Esempi di stati "stressati" sono l'overload, il surriscaldato e così via.

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (5)


</dt> <dd>

Un elemento funziona nominalmente, ma prevede un guasto nel prossimo futuro.

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (6)


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore non ripristinabile** (7)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (8)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** (9)


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (10)


</dt> <dd>

Si è verificata un'interruzione ordinata.

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In servizio** (11)


</dt> <dd>

Elemento configurato, gestito, pulito o amministrato in altro modo.

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (12)


</dt> <dd>

Il sistema di monitoraggio è a conoscenza di questo elemento, ma non è mai stato in grado di stabilire comunicazioni con esso.

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (13)


</dt> <dd>

È noto che l'elemento ManagedSystem esiste ed è stato contattato correttamente in passato, ma non è attualmente raggiungibile.

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (14)


</dt> <dd>

Arresto improvviso, in cui potrebbe essere necessario aggiornare lo stato e la configurazione dell'elemento.

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattiva** (15)


</dt> <dd>

L'elemento è inattivo o inattivo.

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (16)


</dt> <dd>

Questo elemento potrebbe essere "OK", ma un altro elemento, da cui dipende, è in errore. Un esempio è un servizio di rete o un endpoint che non può funzionare a causa di problemi di rete di livello inferiore.

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (17)


</dt> <dd>

L'elemento ha completato l'operazione.

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Modalità risparmio energia** (18)


</dt> <dd>

L'elemento contiene informazioni aggiuntive sul modello di potenza contenute nell'associazione PowerManagementService associata.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (0x8000.)


</dt> <dd></dd> </dl>

</dd> <dt>

**Stato primario**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**DetailedStatus**", "**CIM \_ ManagedSystemElement**.**HealthState**")
</dt> </dl>

Indica un valore di stato di alto livello.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Danneggiato** (2)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (0x8000.)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ ManagedSystemElement**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Indica lo stato primario dell'oggetto.

> [!Note]  
> Questa proprietà è deprecata. Viene sostituito dalla **proprietà OperationalStatus.** Se si sceglie di usare la **proprietà Status per** la compatibilità con le versioni precedenti, deve essere secondaria alla proprietà **OperationalStatus.**

 

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> <dt>



 ("Stressed")


</dt> <dd></dd> <dt>



 ("NonRecover")


</dt> <dd></dd> <dt>



 ("Nessun contatto")


</dt> <dd></dd> <dt>



 ("Lost Comm")


</dt> <dd></dd> <dt>



 ("Arrestato")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**OperationalStatus**")
</dt> </dl>

Indica le descrizioni dei valori corrispondenti nella **matrice OperationalStatus.** Ad esempio, se un elemento nella proprietà **OperationalStatus** contiene il valore **Stopping**, l'elemento in corrispondenza dello stesso indice di matrice in questa proprietà potrebbe contenere una spiegazione del motivo per cui un oggetto viene arrestato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

